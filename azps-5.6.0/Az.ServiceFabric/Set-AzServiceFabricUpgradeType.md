---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c117937d674c95f69eb967667c86c503ffbb62c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976318"
---
# <span data-ttu-id="729ca-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="729ca-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="729ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="729ca-102">SYNOPSIS</span></span>
<span data-ttu-id="729ca-103">Modificare il tipo di aggiornamento Service Fabric del cluster.</span><span class="sxs-lookup"><span data-stu-id="729ca-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="729ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="729ca-104">SYNTAX</span></span>

### <span data-ttu-id="729ca-105">Automatico</span><span class="sxs-lookup"><span data-stu-id="729ca-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ca-106">Manuale</span><span class="sxs-lookup"><span data-stu-id="729ca-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729ca-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="729ca-107">DESCRIPTION</span></span>
<span data-ttu-id="729ca-108">Usare **Set-AzServiceFabricUpgradeType** per impostare il tipo di aggiornamento su automatico o manuale con una specifica versione del codice Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="729ca-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="729ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="729ca-109">EXAMPLES</span></span>

### <span data-ttu-id="729ca-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="729ca-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="729ca-111">Questo comando imposta la modalità di aggiornamento del cluster su automatica.</span><span class="sxs-lookup"><span data-stu-id="729ca-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="729ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="729ca-112">PARAMETERS</span></span>

### <span data-ttu-id="729ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729ca-113">-DefaultProfile</span></span>
<span data-ttu-id="729ca-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="729ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="729ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="729ca-115">-Name</span></span>
<span data-ttu-id="729ca-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="729ca-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="729ca-118">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="729ca-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="729ca-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="729ca-119">-UpgradeMode</span></span>
<span data-ttu-id="729ca-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="729ca-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729ca-121">-Version</span><span class="sxs-lookup"><span data-stu-id="729ca-121">-Version</span></span>
<span data-ttu-id="729ca-122">Versione del codice cluster</span><span class="sxs-lookup"><span data-stu-id="729ca-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729ca-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="729ca-123">-Confirm</span></span>
<span data-ttu-id="729ca-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="729ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729ca-125">-WhatIf</span></span>
<span data-ttu-id="729ca-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="729ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="729ca-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="729ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729ca-128">CommonParameters</span></span>
<span data-ttu-id="729ca-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729ca-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="729ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729ca-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="729ca-131">INPUTS</span></span>

### <span data-ttu-id="729ca-132">System.String</span><span class="sxs-lookup"><span data-stu-id="729ca-132">System.String</span></span>

### <span data-ttu-id="729ca-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="729ca-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="729ca-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="729ca-134">OUTPUTS</span></span>

### <span data-ttu-id="729ca-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="729ca-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="729ca-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="729ca-136">NOTES</span></span>

## <span data-ttu-id="729ca-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="729ca-137">RELATED LINKS</span></span>
