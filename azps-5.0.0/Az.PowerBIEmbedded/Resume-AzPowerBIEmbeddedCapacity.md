---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200323"
---
# <span data-ttu-id="22cc2-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22cc2-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="22cc2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="22cc2-103">Riprende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="22cc2-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="22cc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22cc2-104">SYNTAX</span></span>

### <span data-ttu-id="22cc2-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22cc2-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cc2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22cc2-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cc2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="22cc2-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cc2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="22cc2-109">Il cmdlet Resume-AzPowerBIEmbeddedCapacity riprende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="22cc2-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="22cc2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22cc2-110">EXAMPLES</span></span>

### <span data-ttu-id="22cc2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22cc2-111">Example 1</span></span>
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

<span data-ttu-id="22cc2-112">Questo comando riprenderà una capacità sospesa denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="22cc2-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="22cc2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22cc2-113">PARAMETERS</span></span>

### <span data-ttu-id="22cc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cc2-114">-DefaultProfile</span></span>
<span data-ttu-id="22cc2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22cc2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cc2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22cc2-116">-InputObject</span></span>
<span data-ttu-id="22cc2-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="22cc2-117">Input object for Piping</span></span>

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

### <span data-ttu-id="22cc2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="22cc2-118">-Name</span></span>
<span data-ttu-id="22cc2-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="22cc2-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="22cc2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22cc2-120">-PassThru</span></span>
<span data-ttu-id="22cc2-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="22cc2-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="22cc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="22cc2-123">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="22cc2-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="22cc2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22cc2-124">-ResourceId</span></span>
<span data-ttu-id="22cc2-125">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="22cc2-125">Azure resource ID</span></span>

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

### <span data-ttu-id="22cc2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22cc2-126">-Confirm</span></span>
<span data-ttu-id="22cc2-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="22cc2-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="22cc2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cc2-128">-WhatIf</span></span>
<span data-ttu-id="22cc2-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="22cc2-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="22cc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cc2-130">CommonParameters</span></span>
<span data-ttu-id="22cc2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cc2-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cc2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cc2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22cc2-133">INPUTS</span></span>

### <span data-ttu-id="22cc2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22cc2-134">System.String</span></span>

### <span data-ttu-id="22cc2-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22cc2-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="22cc2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22cc2-136">OUTPUTS</span></span>

### <span data-ttu-id="22cc2-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22cc2-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="22cc2-138">Note</span><span class="sxs-lookup"><span data-stu-id="22cc2-138">NOTES</span></span>

## <span data-ttu-id="22cc2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22cc2-139">RELATED LINKS</span></span>

[<span data-ttu-id="22cc2-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22cc2-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="22cc2-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22cc2-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
