---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516895"
---
# <span data-ttu-id="35019-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="35019-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="35019-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35019-102">SYNOPSIS</span></span>
<span data-ttu-id="35019-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="35019-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35019-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35019-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="35019-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35019-105">DESCRIPTION</span></span>
<span data-ttu-id="35019-106">Il cmdlet **Get-AzureRmContainerService** ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="35019-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="35019-107">È possibile visualizzare le proprietà di un servizio contenitore, che include lo stato, il numero di master e gli agenti e il nome di dominio completo di master e Agent.</span><span class="sxs-lookup"><span data-stu-id="35019-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="35019-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35019-108">EXAMPLES</span></span>

### <span data-ttu-id="35019-109">Esempio 1: ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="35019-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="35019-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="35019-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="35019-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35019-111">PARAMETERS</span></span>

### <span data-ttu-id="35019-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="35019-112">-Name</span></span>
<span data-ttu-id="35019-113">Specifica il nome del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35019-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35019-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35019-114">-ResourceGroupName</span></span>
<span data-ttu-id="35019-115">Specifica il gruppo di risorse del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35019-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35019-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35019-116">CommonParameters</span></span>
<span data-ttu-id="35019-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35019-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35019-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35019-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35019-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35019-119">INPUTS</span></span>

### <span data-ttu-id="35019-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35019-120">None</span></span>
<span data-ttu-id="35019-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="35019-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35019-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35019-122">OUTPUTS</span></span>

## <span data-ttu-id="35019-123">Note</span><span class="sxs-lookup"><span data-stu-id="35019-123">NOTES</span></span>

## <span data-ttu-id="35019-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35019-124">RELATED LINKS</span></span>

[<span data-ttu-id="35019-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="35019-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="35019-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="35019-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="35019-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="35019-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


