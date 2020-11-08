---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023628"
---
# <span data-ttu-id="ef9b9-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="ef9b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9b9-103">Ottiene un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="ef9b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef9b9-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ef9b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef9b9-106">Il cmdlet **Get-AzureApplicationGateway** ottiene un gateway di applicazione Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="ef9b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef9b9-108">Esempio 1: ottenere un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ef9b9-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="ef9b9-109">Questo comando consente di ottenere il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="ef9b9-110">Esempio 2: ottenere tutti i gateway delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="ef9b9-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="ef9b9-111">Questo comando consente di ottenere tutti i gateway dell'applicazione sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="ef9b9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef9b9-112">PARAMETERS</span></span>

### <span data-ttu-id="ef9b9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef9b9-113">-Name</span></span>
<span data-ttu-id="ef9b9-114">Specifica il nome del gateway dell'applicazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b9-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef9b9-115">-Profile</span></span>
<span data-ttu-id="ef9b9-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ef9b9-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef9b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9b9-118">CommonParameters</span></span>
<span data-ttu-id="ef9b9-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9b9-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9b9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9b9-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef9b9-121">INPUTS</span></span>

### <span data-ttu-id="ef9b9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ef9b9-122">System.String</span></span>

## <span data-ttu-id="ef9b9-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef9b9-123">OUTPUTS</span></span>

### <span data-ttu-id="ef9b9-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="ef9b9-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="ef9b9-125">Note</span><span class="sxs-lookup"><span data-stu-id="ef9b9-125">NOTES</span></span>

## <span data-ttu-id="ef9b9-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef9b9-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef9b9-127">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="ef9b9-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="ef9b9-129">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="ef9b9-130">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="ef9b9-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef9b9-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


