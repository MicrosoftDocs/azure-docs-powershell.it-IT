---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511899"
---
# <span data-ttu-id="e7444-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e7444-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="e7444-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7444-102">SYNOPSIS</span></span>
<span data-ttu-id="e7444-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e7444-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7444-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7444-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7444-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7444-105">DESCRIPTION</span></span>
<span data-ttu-id="e7444-106">Il cmdlet **Get-AzureRmContainerService** ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e7444-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="e7444-107">È possibile visualizzare le proprietà di un servizio contenitore, che include lo stato, il numero di master e gli agenti e il nome di dominio completo di master e Agent.</span><span class="sxs-lookup"><span data-stu-id="e7444-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="e7444-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7444-108">EXAMPLES</span></span>

### <span data-ttu-id="e7444-109">Esempio 1: ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="e7444-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e7444-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e7444-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="e7444-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7444-111">PARAMETERS</span></span>

### <span data-ttu-id="e7444-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7444-112">-DefaultProfile</span></span>
<span data-ttu-id="e7444-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7444-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7444-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7444-114">-Name</span></span>
<span data-ttu-id="e7444-115">Specifica il nome del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7444-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7444-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7444-116">-ResourceGroupName</span></span>
<span data-ttu-id="e7444-117">Specifica il gruppo di risorse del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7444-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7444-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7444-118">CommonParameters</span></span>
<span data-ttu-id="e7444-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7444-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7444-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7444-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7444-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7444-121">INPUTS</span></span>

### <span data-ttu-id="e7444-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e7444-122">System.String</span></span>

## <span data-ttu-id="e7444-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7444-123">OUTPUTS</span></span>

### <span data-ttu-id="e7444-124">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e7444-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e7444-125">Note</span><span class="sxs-lookup"><span data-stu-id="e7444-125">NOTES</span></span>

## <span data-ttu-id="e7444-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7444-126">RELATED LINKS</span></span>

[<span data-ttu-id="e7444-127">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e7444-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="e7444-128">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e7444-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="e7444-129">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e7444-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


