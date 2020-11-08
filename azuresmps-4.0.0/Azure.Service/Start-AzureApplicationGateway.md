---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023737"
---
# <span data-ttu-id="07fa3-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="07fa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="07fa3-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="07fa3-103">Starts an application gateway.</span></span>

## <span data-ttu-id="07fa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07fa3-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07fa3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="07fa3-106">Il cmdlet **Start-AzureApplicationGateway** avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="07fa3-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="07fa3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="07fa3-108">Esempio 1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="07fa3-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="07fa3-109">Questo comando avvia il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="07fa3-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="07fa3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="07fa3-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="07fa3-111">-Name</span></span>
<span data-ttu-id="07fa3-112">Specifica il nome del gateway dell'applicazione che questo cmdlet avvia.</span><span class="sxs-lookup"><span data-stu-id="07fa3-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fa3-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="07fa3-113">-Profile</span></span>
<span data-ttu-id="07fa3-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07fa3-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="07fa3-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="07fa3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fa3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fa3-116">CommonParameters</span></span>
<span data-ttu-id="07fa3-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fa3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fa3-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fa3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fa3-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07fa3-119">INPUTS</span></span>

### <span data-ttu-id="07fa3-120">System. String</span><span class="sxs-lookup"><span data-stu-id="07fa3-120">System.String</span></span>

## <span data-ttu-id="07fa3-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07fa3-121">OUTPUTS</span></span>

### <span data-ttu-id="07fa3-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="07fa3-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="07fa3-123">Note</span><span class="sxs-lookup"><span data-stu-id="07fa3-123">NOTES</span></span>

## <span data-ttu-id="07fa3-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07fa3-124">RELATED LINKS</span></span>

[<span data-ttu-id="07fa3-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="07fa3-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="07fa3-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="07fa3-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="07fa3-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07fa3-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


