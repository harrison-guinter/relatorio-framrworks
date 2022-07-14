Os frameworks funcionam como um modelo para a criação de softwares e aplicativos. Eles oferecem uma série de estruturas básicas que facilitam o trabalho do programador. Por oferecerem uma estrutura base para agilizar o desenvolvimento, os frameworks dão a vantagem de não começar o desenvolvimento completamente do zero.

<?php
 
namespace App\Mail;
 
use App\Models\Order;
use Illuminate\Bus\Queueable;
use Illuminate\Mail\Mailable;
use Illuminate\Queue\SerializesModels;
 
class OrderShipped extends Mailable
{
    use Queueable, SerializesModels;
     public $order;
     public function __construct(Order $order)
    {
        $this->order = $order;
    }
     public function build()
    {
        return $this->view('emails.orders.shipped');
    }
}
