---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515144"
---
# <span data-ttu-id="a4aac-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a4aac-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="a4aac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4aac-102">SYNOPSIS</span></span>
<span data-ttu-id="a4aac-103">Imposta le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4aac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4aac-104">SYNTAX</span></span>

### <span data-ttu-id="a4aac-105">SetByIndividualParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4aac-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4aac-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4aac-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4aac-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a4aac-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4aac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4aac-108">DESCRIPTION</span></span>
<span data-ttu-id="a4aac-109">Imposta tutte le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="a4aac-110">Poiché imposta tutte le proprietà quando si usa un oggetto cluster, è necessario che venga passato un oggetto di input completamente valido.</span><span class="sxs-lookup"><span data-stu-id="a4aac-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="a4aac-111">Le proprietà di sola lettura verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="a4aac-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="a4aac-112">Solo alcune proprietà sono attualmente aggiornabili, come illustrato nei set di parametri.</span><span class="sxs-lookup"><span data-stu-id="a4aac-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="a4aac-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4aac-113">EXAMPLES</span></span>

### <span data-ttu-id="a4aac-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4aac-114">Example 1</span></span>
<span data-ttu-id="a4aac-115">Aggiornare un cluster usando singoli parametri.</span><span class="sxs-lookup"><span data-stu-id="a4aac-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="a4aac-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a4aac-116">Example 2</span></span>
<span data-ttu-id="a4aac-117">Aggiornare un cluster usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="a4aac-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="a4aac-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4aac-118">PARAMETERS</span></span>

### <span data-ttu-id="a4aac-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="a4aac-119">-AgentCount</span></span>
<span data-ttu-id="a4aac-120">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a4aac-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="a4aac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4aac-121">-DefaultProfile</span></span>
<span data-ttu-id="a4aac-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4aac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4aac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4aac-123">-InputObject</span></span>
<span data-ttu-id="a4aac-124">Proprietà del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-124">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="a4aac-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4aac-125">-Name</span></span>
<span data-ttu-id="a4aac-126">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-126">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="a4aac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4aac-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4aac-128">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-128">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a4aac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4aac-129">-ResourceId</span></span>
<span data-ttu-id="a4aac-130">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="a4aac-130">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a4aac-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a4aac-131">-SslCertificate</span></span>
<span data-ttu-id="a4aac-132">Dati del certificato SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="a4aac-132">The SSL certificate data in PEM format.</span></span>

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

### <span data-ttu-id="a4aac-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="a4aac-133">-SslCName</span></span>
<span data-ttu-id="a4aac-134">Il CName per il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a4aac-134">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="a4aac-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="a4aac-135">-SslKey</span></span>
<span data-ttu-id="a4aac-136">Dati della chiave SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="a4aac-136">The SSL key data in PEM format.</span></span>

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

### <span data-ttu-id="a4aac-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="a4aac-137">-SslStatus</span></span>
<span data-ttu-id="a4aac-138">Stato SSL.</span><span class="sxs-lookup"><span data-stu-id="a4aac-138">SSL status.</span></span>
<span data-ttu-id="a4aac-139">I valori possibili sono "Enabled" e "disabled".</span><span class="sxs-lookup"><span data-stu-id="a4aac-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="a4aac-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4aac-140">-Confirm</span></span>
<span data-ttu-id="a4aac-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4aac-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4aac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4aac-142">-WhatIf</span></span>
<span data-ttu-id="a4aac-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4aac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4aac-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4aac-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4aac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4aac-145">CommonParameters</span></span>
<span data-ttu-id="a4aac-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4aac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4aac-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4aac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4aac-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4aac-148">INPUTS</span></span>

### <span data-ttu-id="a4aac-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a4aac-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="a4aac-150">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4aac-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a4aac-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a4aac-151">System.String</span></span>

### <span data-ttu-id="a4aac-152">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a4aac-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a4aac-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4aac-153">OUTPUTS</span></span>

### <span data-ttu-id="a4aac-154">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a4aac-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="a4aac-155">Note</span><span class="sxs-lookup"><span data-stu-id="a4aac-155">NOTES</span></span>

## <span data-ttu-id="a4aac-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4aac-156">RELATED LINKS</span></span>
