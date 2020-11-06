---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 29113eecc02443fe2fbc8f57ada1fcfa8e7a2d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511580"
---
# <span data-ttu-id="db82b-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db82b-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="db82b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db82b-102">SYNOPSIS</span></span>
<span data-ttu-id="db82b-103">Riprende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="db82b-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db82b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db82b-104">SYNTAX</span></span>

### <span data-ttu-id="db82b-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db82b-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db82b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db82b-106">ByResourceId</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db82b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db82b-107">ByInputObject</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db82b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db82b-108">DESCRIPTION</span></span>
<span data-ttu-id="db82b-109">Il cmdlet Resume-AzureRmPowerBIEmbeddedCapacity riprende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="db82b-109">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="db82b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db82b-110">EXAMPLES</span></span>

### <span data-ttu-id="db82b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db82b-111">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="db82b-112">Questo comando riprenderà una capacità sospesa denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="db82b-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="db82b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db82b-113">PARAMETERS</span></span>

### <span data-ttu-id="db82b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db82b-114">-DefaultProfile</span></span>
<span data-ttu-id="db82b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db82b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db82b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db82b-116">-InputObject</span></span>
<span data-ttu-id="db82b-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="db82b-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db82b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="db82b-118">-Name</span></span>
<span data-ttu-id="db82b-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="db82b-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db82b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db82b-120">-PassThru</span></span>
<span data-ttu-id="db82b-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="db82b-121">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db82b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db82b-122">-ResourceGroupName</span></span>
<span data-ttu-id="db82b-123">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="db82b-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db82b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db82b-124">-ResourceId</span></span>
<span data-ttu-id="db82b-125">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="db82b-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db82b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db82b-126">-Confirm</span></span>
<span data-ttu-id="db82b-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="db82b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="db82b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db82b-128">-WhatIf</span></span>
<span data-ttu-id="db82b-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="db82b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="db82b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db82b-130">CommonParameters</span></span>
<span data-ttu-id="db82b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db82b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db82b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db82b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db82b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db82b-133">INPUTS</span></span>

### <span data-ttu-id="db82b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="db82b-134">System.String</span></span>

### <span data-ttu-id="db82b-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db82b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="db82b-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db82b-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="db82b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db82b-137">OUTPUTS</span></span>

### <span data-ttu-id="db82b-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db82b-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="db82b-139">Note</span><span class="sxs-lookup"><span data-stu-id="db82b-139">NOTES</span></span>

## <span data-ttu-id="db82b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db82b-140">RELATED LINKS</span></span>

[<span data-ttu-id="db82b-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db82b-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="db82b-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db82b-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
