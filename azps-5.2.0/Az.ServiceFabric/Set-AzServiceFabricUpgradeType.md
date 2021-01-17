---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345460"
---
# <span data-ttu-id="de25f-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="de25f-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="de25f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de25f-102">SYNOPSIS</span></span>
<span data-ttu-id="de25f-103">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="de25f-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="de25f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de25f-104">SYNTAX</span></span>

### <span data-ttu-id="de25f-105">Automatico</span><span class="sxs-lookup"><span data-stu-id="de25f-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de25f-106">Manuale</span><span class="sxs-lookup"><span data-stu-id="de25f-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de25f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de25f-107">DESCRIPTION</span></span>
<span data-ttu-id="de25f-108">Usare **set-AzServiceFabricUpgradeType** per impostare il tipo di aggiornamento su automatico o manuale con una versione specifica del codice del tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="de25f-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="de25f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de25f-109">EXAMPLES</span></span>

### <span data-ttu-id="de25f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de25f-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="de25f-111">Questo comando consentirà di impostare la modalità di aggiornamento del cluster su automatica.</span><span class="sxs-lookup"><span data-stu-id="de25f-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="de25f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de25f-112">PARAMETERS</span></span>

### <span data-ttu-id="de25f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de25f-113">-DefaultProfile</span></span>
<span data-ttu-id="de25f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de25f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de25f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="de25f-115">-Name</span></span>
<span data-ttu-id="de25f-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="de25f-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="de25f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de25f-117">-ResourceGroupName</span></span>
<span data-ttu-id="de25f-118">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de25f-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="de25f-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="de25f-119">-UpgradeMode</span></span>
<span data-ttu-id="de25f-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="de25f-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="de25f-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="de25f-121">-Version</span></span>
<span data-ttu-id="de25f-122">Versione del codice del cluster</span><span class="sxs-lookup"><span data-stu-id="de25f-122">Cluster code version</span></span>

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

### <span data-ttu-id="de25f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de25f-123">-Confirm</span></span>
<span data-ttu-id="de25f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de25f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de25f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de25f-125">-WhatIf</span></span>
<span data-ttu-id="de25f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de25f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de25f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de25f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de25f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de25f-128">CommonParameters</span></span>
<span data-ttu-id="de25f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de25f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de25f-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de25f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de25f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de25f-131">INPUTS</span></span>

### <span data-ttu-id="de25f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="de25f-132">System.String</span></span>

### <span data-ttu-id="de25f-133">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="de25f-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="de25f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de25f-134">OUTPUTS</span></span>

### <span data-ttu-id="de25f-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="de25f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="de25f-136">Note</span><span class="sxs-lookup"><span data-stu-id="de25f-136">NOTES</span></span>

## <span data-ttu-id="de25f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de25f-137">RELATED LINKS</span></span>
