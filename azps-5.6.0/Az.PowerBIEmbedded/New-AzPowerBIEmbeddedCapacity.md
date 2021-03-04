---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 86531beb13ef70f8c35de7f4921277b0f9fa0bf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953454"
---
# <span data-ttu-id="4093c-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4093c-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4093c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4093c-102">SYNOPSIS</span></span>
<span data-ttu-id="4093c-103">Crea una nuova capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4093c-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4093c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4093c-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4093c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4093c-105">DESCRIPTION</span></span>
<span data-ttu-id="4093c-106">Il cmdlet New-AzPowerBIEmbeddedCapacity crea una nuova capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4093c-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4093c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4093c-107">EXAMPLES</span></span>

### <span data-ttu-id="4093c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4093c-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="4093c-109">Crea una capacità denominata testcapacity nell'area azure centrale di Azure e nel testRG del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4093c-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="4093c-110">Il livello di SKU per la capacità sarà A1.</span><span class="sxs-lookup"><span data-stu-id="4093c-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="4093c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4093c-111">PARAMETERS</span></span>

### <span data-ttu-id="4093c-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="4093c-112">-Administrator</span></span>
<span data-ttu-id="4093c-113">Nomi separati da virgola da impostare come amministratori della capacità</span><span class="sxs-lookup"><span data-stu-id="4093c-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4093c-114">-DefaultProfile</span></span>
<span data-ttu-id="4093c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4093c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4093c-116">-Location</span></span>
<span data-ttu-id="4093c-117">Area geografica di Azure in cui è ospitata la capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4093c-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4093c-118">-Name</span></span>
<span data-ttu-id="4093c-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4093c-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4093c-120">-ResourceGroupName</span></span>
<span data-ttu-id="4093c-121">Nome del gruppo di risorse azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="4093c-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="4093c-122">-Sku</span></span>
<span data-ttu-id="4093c-123">Nome della SKU per la capacità.</span><span class="sxs-lookup"><span data-stu-id="4093c-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4093c-124">-Tag</span></span>
<span data-ttu-id="4093c-125">Coppie chiave-valore sotto forma di tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="4093c-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4093c-126">-Confirm</span></span>
<span data-ttu-id="4093c-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="4093c-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4093c-128">-WhatIf</span></span>
<span data-ttu-id="4093c-129">Descrive le azioni che l'operazione corrente eseguirà senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="4093c-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4093c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4093c-130">CommonParameters</span></span>
<span data-ttu-id="4093c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4093c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4093c-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4093c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4093c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="4093c-133">INPUTS</span></span>

### <span data-ttu-id="4093c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4093c-134">System.String</span></span>

### <span data-ttu-id="4093c-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4093c-135">System.String[]</span></span>

### <span data-ttu-id="4093c-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4093c-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4093c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4093c-137">OUTPUTS</span></span>

### <span data-ttu-id="4093c-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4093c-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4093c-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="4093c-139">NOTES</span></span>

## <span data-ttu-id="4093c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4093c-140">RELATED LINKS</span></span>

[<span data-ttu-id="4093c-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4093c-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4093c-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4093c-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
