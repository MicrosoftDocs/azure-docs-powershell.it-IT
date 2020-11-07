---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835268"
---
# <span data-ttu-id="f9570-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9570-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="f9570-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9570-102">SYNOPSIS</span></span>
<span data-ttu-id="f9570-103">Imposta le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="f9570-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9570-104">SYNTAX</span></span>

### <span data-ttu-id="f9570-105">SetByIndividualParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9570-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9570-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9570-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9570-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9570-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9570-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9570-108">DESCRIPTION</span></span>
<span data-ttu-id="f9570-109">Imposta tutte le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="f9570-110">Poiché imposta tutte le proprietà quando si usa un oggetto cluster, è necessario che venga passato un oggetto di input completamente valido.</span><span class="sxs-lookup"><span data-stu-id="f9570-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="f9570-111">Le proprietà di sola lettura verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="f9570-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="f9570-112">Solo alcune proprietà sono attualmente aggiornabili, come illustrato nei set di parametri.</span><span class="sxs-lookup"><span data-stu-id="f9570-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="f9570-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9570-113">EXAMPLES</span></span>

### <span data-ttu-id="f9570-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9570-114">Example 1</span></span>
<span data-ttu-id="f9570-115">Aggiornare un cluster usando singoli parametri.</span><span class="sxs-lookup"><span data-stu-id="f9570-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="f9570-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f9570-116">Example 2</span></span>
<span data-ttu-id="f9570-117">Aggiornare un cluster usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="f9570-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="f9570-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9570-118">PARAMETERS</span></span>

### <span data-ttu-id="f9570-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="f9570-119">-AgentCount</span></span>
<span data-ttu-id="f9570-120">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f9570-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9570-121">-DefaultProfile</span></span>
<span data-ttu-id="f9570-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9570-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9570-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9570-123">-InputObject</span></span>
<span data-ttu-id="f9570-124">Proprietà del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9570-125">-Name</span></span>
<span data-ttu-id="f9570-126">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9570-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9570-128">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9570-129">-ResourceId</span></span>
<span data-ttu-id="f9570-130">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f9570-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9570-131">-SslCertificate</span></span>
<span data-ttu-id="f9570-132">Dati del certificato SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="f9570-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="f9570-133">-SslCName</span></span>
<span data-ttu-id="f9570-134">Il CName per il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="f9570-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="f9570-135">-SslKey</span></span>
<span data-ttu-id="f9570-136">Dati della chiave SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="f9570-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="f9570-137">-SslStatus</span></span>
<span data-ttu-id="f9570-138">Stato SSL.</span><span class="sxs-lookup"><span data-stu-id="f9570-138">SSL status.</span></span>
<span data-ttu-id="f9570-139">I valori possibili sono "Enabled" e "disabled".</span><span class="sxs-lookup"><span data-stu-id="f9570-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9570-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9570-140">-Confirm</span></span>
<span data-ttu-id="f9570-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9570-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9570-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9570-142">-WhatIf</span></span>
<span data-ttu-id="f9570-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9570-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9570-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9570-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9570-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9570-145">CommonParameters</span></span>
<span data-ttu-id="f9570-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9570-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9570-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9570-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9570-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9570-148">INPUTS</span></span>

### <span data-ttu-id="f9570-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f9570-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="f9570-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f9570-150">System.String</span></span>

### <span data-ttu-id="f9570-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f9570-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f9570-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9570-152">OUTPUTS</span></span>

### <span data-ttu-id="f9570-153">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f9570-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="f9570-154">Note</span><span class="sxs-lookup"><span data-stu-id="f9570-154">NOTES</span></span>

## <span data-ttu-id="f9570-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9570-155">RELATED LINKS</span></span>
