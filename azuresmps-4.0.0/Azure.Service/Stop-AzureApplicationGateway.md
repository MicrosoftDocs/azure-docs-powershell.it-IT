---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029870"
---
# <span data-ttu-id="74f41-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="74f41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74f41-102">SYNOPSIS</span></span>
<span data-ttu-id="74f41-103">Arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74f41-103">Stops an application gateway.</span></span>

## <span data-ttu-id="74f41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74f41-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74f41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74f41-105">DESCRIPTION</span></span>
<span data-ttu-id="74f41-106">Il cmdlet **Stop-AzureApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74f41-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="74f41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74f41-107">EXAMPLES</span></span>

### <span data-ttu-id="74f41-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="74f41-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="74f41-109">Questo comando Arresta il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="74f41-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="74f41-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74f41-110">PARAMETERS</span></span>

### <span data-ttu-id="74f41-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="74f41-111">-Name</span></span>
<span data-ttu-id="74f41-112">Specifica il nome del gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="74f41-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="74f41-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="74f41-113">-Profile</span></span>
<span data-ttu-id="74f41-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74f41-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74f41-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="74f41-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74f41-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f41-116">CommonParameters</span></span>
<span data-ttu-id="74f41-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f41-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f41-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f41-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f41-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74f41-119">INPUTS</span></span>

### <span data-ttu-id="74f41-120">System. String</span><span class="sxs-lookup"><span data-stu-id="74f41-120">System.String</span></span>

## <span data-ttu-id="74f41-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74f41-121">OUTPUTS</span></span>

### <span data-ttu-id="74f41-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="74f41-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="74f41-123">Note</span><span class="sxs-lookup"><span data-stu-id="74f41-123">NOTES</span></span>

## <span data-ttu-id="74f41-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74f41-124">RELATED LINKS</span></span>

[<span data-ttu-id="74f41-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="74f41-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="74f41-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="74f41-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="74f41-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f41-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
