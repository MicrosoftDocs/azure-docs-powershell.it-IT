---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021501"
---
# <span data-ttu-id="9ae42-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9ae42-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9ae42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ae42-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae42-103">Riprende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="9ae42-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="9ae42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae42-104">SYNTAX</span></span>

### <span data-ttu-id="9ae42-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ae42-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae42-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae42-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae42-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ae42-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae42-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ae42-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae42-109">Il cmdlet Resume-AzPowerBIEmbeddedCapacity riprende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="9ae42-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="9ae42-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae42-110">EXAMPLES</span></span>

### <span data-ttu-id="9ae42-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ae42-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="9ae42-112">Questo comando riprenderà una capacità sospesa denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="9ae42-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="9ae42-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ae42-113">PARAMETERS</span></span>

### <span data-ttu-id="9ae42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae42-114">-DefaultProfile</span></span>
<span data-ttu-id="9ae42-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae42-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae42-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ae42-116">-InputObject</span></span>
<span data-ttu-id="9ae42-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="9ae42-117">Input object for Piping</span></span>

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

### <span data-ttu-id="9ae42-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ae42-118">-Name</span></span>
<span data-ttu-id="9ae42-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="9ae42-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="9ae42-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae42-120">-PassThru</span></span>
<span data-ttu-id="9ae42-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9ae42-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ae42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae42-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ae42-123">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="9ae42-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="9ae42-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae42-124">-ResourceId</span></span>
<span data-ttu-id="9ae42-125">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="9ae42-125">Azure resource ID</span></span>

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

### <span data-ttu-id="9ae42-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ae42-126">-Confirm</span></span>
<span data-ttu-id="9ae42-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="9ae42-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9ae42-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae42-128">-WhatIf</span></span>
<span data-ttu-id="9ae42-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="9ae42-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9ae42-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae42-130">CommonParameters</span></span>
<span data-ttu-id="9ae42-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae42-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae42-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae42-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae42-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ae42-133">INPUTS</span></span>

### <span data-ttu-id="9ae42-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ae42-134">System.String</span></span>

### <span data-ttu-id="9ae42-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9ae42-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9ae42-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae42-136">OUTPUTS</span></span>

### <span data-ttu-id="9ae42-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9ae42-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9ae42-138">Note</span><span class="sxs-lookup"><span data-stu-id="9ae42-138">NOTES</span></span>

## <span data-ttu-id="9ae42-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae42-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ae42-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9ae42-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="9ae42-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9ae42-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
