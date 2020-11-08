---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029959"
---
# <span data-ttu-id="3d34a-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="3d34a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d34a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d34a-103">Rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d34a-103">Removes an application gateway.</span></span>

## <span data-ttu-id="3d34a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d34a-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d34a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d34a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d34a-106">Il cmdlet **Remove-AzureApplicationGateway** rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d34a-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="3d34a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d34a-107">EXAMPLES</span></span>

### <span data-ttu-id="3d34a-108">Esempio 1: rimuovere un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3d34a-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="3d34a-109">Questo comando rimuove il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="3d34a-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="3d34a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d34a-110">PARAMETERS</span></span>

### <span data-ttu-id="3d34a-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d34a-111">-Name</span></span>
<span data-ttu-id="3d34a-112">Specifica il nome del gateway dell'applicazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d34a-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d34a-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d34a-113">-Profile</span></span>
<span data-ttu-id="3d34a-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d34a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3d34a-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3d34a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d34a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d34a-116">CommonParameters</span></span>
<span data-ttu-id="3d34a-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d34a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d34a-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d34a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d34a-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d34a-119">INPUTS</span></span>

### <span data-ttu-id="3d34a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3d34a-120">System.String</span></span>

## <span data-ttu-id="3d34a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d34a-121">OUTPUTS</span></span>

### <span data-ttu-id="3d34a-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3d34a-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="3d34a-123">Note</span><span class="sxs-lookup"><span data-stu-id="3d34a-123">NOTES</span></span>

## <span data-ttu-id="3d34a-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d34a-124">RELATED LINKS</span></span>

[<span data-ttu-id="3d34a-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="3d34a-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="3d34a-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="3d34a-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="3d34a-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d34a-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


