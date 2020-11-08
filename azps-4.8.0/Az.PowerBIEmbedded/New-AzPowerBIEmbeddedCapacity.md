---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190883"
---
# <span data-ttu-id="1bc94-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1bc94-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1bc94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bc94-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc94-103">Crea una nuova capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="1bc94-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="1bc94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bc94-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bc94-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc94-106">Il cmdlet New-AzPowerBIEmbeddedCapacity crea una nuova capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="1bc94-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1bc94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bc94-107">EXAMPLES</span></span>

### <span data-ttu-id="1bc94-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1bc94-108">Example 1</span></span>
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

<span data-ttu-id="1bc94-109">Crea una capacità denominata testcapacity in Azure Region West Central US e nel gruppo di risorse testRG.</span><span class="sxs-lookup"><span data-stu-id="1bc94-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="1bc94-110">Il livello SKU per la capacità sarà a1.</span><span class="sxs-lookup"><span data-stu-id="1bc94-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="1bc94-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bc94-111">PARAMETERS</span></span>

### <span data-ttu-id="1bc94-112">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="1bc94-112">-Administrator</span></span>
<span data-ttu-id="1bc94-113">Nomi separati da virgola da impostare come amministratore per la capacità</span><span class="sxs-lookup"><span data-stu-id="1bc94-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="1bc94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc94-114">-DefaultProfile</span></span>
<span data-ttu-id="1bc94-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bc94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bc94-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bc94-116">-Location</span></span>
<span data-ttu-id="1bc94-117">Area di Azure in cui è ospitata la capacità incorporata PowerBI</span><span class="sxs-lookup"><span data-stu-id="1bc94-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="1bc94-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bc94-118">-Name</span></span>
<span data-ttu-id="1bc94-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="1bc94-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="1bc94-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc94-120">-ResourceGroupName</span></span>
<span data-ttu-id="1bc94-121">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="1bc94-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="1bc94-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bc94-122">-Sku</span></span>
<span data-ttu-id="1bc94-123">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="1bc94-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="1bc94-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bc94-124">-Tag</span></span>
<span data-ttu-id="1bc94-125">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="1bc94-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="1bc94-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bc94-126">-Confirm</span></span>
<span data-ttu-id="1bc94-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="1bc94-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="1bc94-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc94-128">-WhatIf</span></span>
<span data-ttu-id="1bc94-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="1bc94-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="1bc94-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc94-130">CommonParameters</span></span>
<span data-ttu-id="1bc94-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc94-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc94-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc94-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc94-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bc94-133">INPUTS</span></span>

### <span data-ttu-id="1bc94-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1bc94-134">System.String</span></span>

### <span data-ttu-id="1bc94-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="1bc94-135">System.String[]</span></span>

### <span data-ttu-id="1bc94-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bc94-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1bc94-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bc94-137">OUTPUTS</span></span>

### <span data-ttu-id="1bc94-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1bc94-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1bc94-139">Note</span><span class="sxs-lookup"><span data-stu-id="1bc94-139">NOTES</span></span>

## <span data-ttu-id="1bc94-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bc94-140">RELATED LINKS</span></span>

[<span data-ttu-id="1bc94-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1bc94-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1bc94-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1bc94-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
