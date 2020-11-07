---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: a82bec40d93b33385dfa9aa2b4a5c5d122e59aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677059"
---
# <span data-ttu-id="170db-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="170db-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="170db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="170db-102">SYNOPSIS</span></span>
<span data-ttu-id="170db-103">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="170db-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="170db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="170db-104">SYNTAX</span></span>

### <span data-ttu-id="170db-105">Automatico</span><span class="sxs-lookup"><span data-stu-id="170db-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170db-106">Manuale</span><span class="sxs-lookup"><span data-stu-id="170db-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170db-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="170db-107">DESCRIPTION</span></span>
<span data-ttu-id="170db-108">Usare **set-AzServiceFabricUpgradeType** per impostare il tipo di aggiornamento su automatico o manuale con una versione specifica del codice del tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="170db-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="170db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="170db-109">EXAMPLES</span></span>

### <span data-ttu-id="170db-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="170db-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="170db-111">Questo comando consentirà di impostare la modalità di aggiornamento del cluster su automatica.</span><span class="sxs-lookup"><span data-stu-id="170db-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="170db-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="170db-112">PARAMETERS</span></span>

### <span data-ttu-id="170db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170db-113">-DefaultProfile</span></span>
<span data-ttu-id="170db-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="170db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170db-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="170db-115">-Name</span></span>
<span data-ttu-id="170db-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="170db-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="170db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170db-117">-ResourceGroupName</span></span>
<span data-ttu-id="170db-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="170db-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="170db-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="170db-119">-UpgradeMode</span></span>
<span data-ttu-id="170db-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="170db-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="170db-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="170db-121">-Version</span></span>
<span data-ttu-id="170db-122">Versione del codice del cluster.</span><span class="sxs-lookup"><span data-stu-id="170db-122">Cluster code version.</span></span>

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

### <span data-ttu-id="170db-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="170db-123">-Confirm</span></span>
<span data-ttu-id="170db-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="170db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170db-125">-WhatIf</span></span>
<span data-ttu-id="170db-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="170db-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="170db-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="170db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170db-128">CommonParameters</span></span>
<span data-ttu-id="170db-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170db-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170db-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="170db-131">INPUTS</span></span>

### <span data-ttu-id="170db-132">System. String</span><span class="sxs-lookup"><span data-stu-id="170db-132">System.String</span></span>

### <span data-ttu-id="170db-133">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="170db-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="170db-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="170db-134">OUTPUTS</span></span>

### <span data-ttu-id="170db-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="170db-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="170db-136">Note</span><span class="sxs-lookup"><span data-stu-id="170db-136">NOTES</span></span>

## <span data-ttu-id="170db-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="170db-137">RELATED LINKS</span></span>
