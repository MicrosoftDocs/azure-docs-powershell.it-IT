---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514952"
---
# <span data-ttu-id="4cd43-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cd43-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4cd43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cd43-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd43-103">Crea una nuova capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4cd43-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cd43-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd43-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cd43-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd43-106">Il cmdlet New-AzureRmPowerBIEmbeddedCapacity crea una nuova capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4cd43-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4cd43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cd43-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd43-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cd43-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="4cd43-109">Crea una capacità denominata testcapacity in Azure Region West Central US e nel gruppo di risorse testRG.</span><span class="sxs-lookup"><span data-stu-id="4cd43-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="4cd43-110">Il livello SKU per la capacità sarà a1.</span><span class="sxs-lookup"><span data-stu-id="4cd43-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="4cd43-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cd43-111">PARAMETERS</span></span>

### <span data-ttu-id="4cd43-112">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="4cd43-112">-Administrator</span></span>
<span data-ttu-id="4cd43-113">Nomi di capacità separati da virgola da impostare come amministratore per la capacità</span><span class="sxs-lookup"><span data-stu-id="4cd43-113">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="4cd43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd43-114">-DefaultProfile</span></span>
<span data-ttu-id="4cd43-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cd43-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4cd43-116">-Location</span></span>
<span data-ttu-id="4cd43-117">Area di Azure in cui è ospitata la capacità incorporata PowerBI</span><span class="sxs-lookup"><span data-stu-id="4cd43-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="4cd43-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cd43-118">-Name</span></span>
<span data-ttu-id="4cd43-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4cd43-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4cd43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd43-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cd43-121">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="4cd43-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4cd43-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="4cd43-122">-Sku</span></span>
<span data-ttu-id="4cd43-123">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="4cd43-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="4cd43-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cd43-124">-Tag</span></span>
<span data-ttu-id="4cd43-125">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="4cd43-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="4cd43-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4cd43-126">-Confirm</span></span>
<span data-ttu-id="4cd43-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="4cd43-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4cd43-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd43-128">-WhatIf</span></span>
<span data-ttu-id="4cd43-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="4cd43-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4cd43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd43-130">CommonParameters</span></span>
<span data-ttu-id="4cd43-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd43-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd43-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd43-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cd43-133">INPUTS</span></span>

### <span data-ttu-id="4cd43-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4cd43-134">System.String</span></span>

### <span data-ttu-id="4cd43-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="4cd43-135">System.String[]</span></span>

### <span data-ttu-id="4cd43-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4cd43-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4cd43-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cd43-137">OUTPUTS</span></span>

### <span data-ttu-id="4cd43-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cd43-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4cd43-139">Note</span><span class="sxs-lookup"><span data-stu-id="4cd43-139">NOTES</span></span>

## <span data-ttu-id="4cd43-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cd43-140">RELATED LINKS</span></span>

[<span data-ttu-id="4cd43-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cd43-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4cd43-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cd43-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
