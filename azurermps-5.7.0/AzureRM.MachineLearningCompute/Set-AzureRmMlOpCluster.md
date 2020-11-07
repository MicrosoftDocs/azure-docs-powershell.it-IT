---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688163"
---
# <span data-ttu-id="17961-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="17961-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="17961-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17961-102">SYNOPSIS</span></span>
<span data-ttu-id="17961-103">Imposta le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17961-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17961-104">SYNTAX</span></span>

### <span data-ttu-id="17961-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="17961-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="17961-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="17961-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="17961-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="17961-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="17961-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17961-108">DESCRIPTION</span></span>
<span data-ttu-id="17961-109">Imposta tutte le proprietà di un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="17961-110">Poiché imposta tutte le proprietà quando si usa un oggetto cluster, è necessario che venga passato un oggetto di input completamente valido.</span><span class="sxs-lookup"><span data-stu-id="17961-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="17961-111">Le proprietà di sola lettura verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="17961-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="17961-112">Solo alcune proprietà sono attualmente aggiornabili, come illustrato nei set di parametri.</span><span class="sxs-lookup"><span data-stu-id="17961-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="17961-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17961-113">EXAMPLES</span></span>

### <span data-ttu-id="17961-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17961-114">Example 1</span></span>
<span data-ttu-id="17961-115">Aggiornare un cluster usando singoli parametri.</span><span class="sxs-lookup"><span data-stu-id="17961-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="17961-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17961-116">Example 2</span></span>
<span data-ttu-id="17961-117">Aggiornare un cluster usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="17961-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="17961-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17961-118">PARAMETERS</span></span>

### <span data-ttu-id="17961-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="17961-119">-AgentCount</span></span>
<span data-ttu-id="17961-120">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="17961-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17961-121">-DefaultProfile</span></span>
<span data-ttu-id="17961-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17961-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17961-123">-InputObject</span></span>
<span data-ttu-id="17961-124">Proprietà del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="17961-125">-Name</span></span>
<span data-ttu-id="17961-126">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17961-127">-ResourceGroupName</span></span>
<span data-ttu-id="17961-128">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17961-129">-ResourceId</span></span>
<span data-ttu-id="17961-130">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="17961-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="17961-131">-SslCertificate</span></span>
<span data-ttu-id="17961-132">Dati del certificato SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="17961-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="17961-133">-SslCName</span></span>
<span data-ttu-id="17961-134">Il CName per il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="17961-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="17961-135">-SslKey</span></span>
<span data-ttu-id="17961-136">Dati della chiave SSL in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="17961-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="17961-137">-SslStatus</span></span>
<span data-ttu-id="17961-138">Stato SSL.</span><span class="sxs-lookup"><span data-stu-id="17961-138">SSL status.</span></span>
<span data-ttu-id="17961-139">I valori possibili sono "Enabled" e "disabled".</span><span class="sxs-lookup"><span data-stu-id="17961-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17961-140">-Confirm</span></span>
<span data-ttu-id="17961-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17961-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17961-142">-WhatIf</span></span>
<span data-ttu-id="17961-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17961-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17961-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17961-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="17961-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17961-145">INPUTS</span></span>

### <span data-ttu-id="17961-146">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="17961-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="17961-147">System. String</span><span class="sxs-lookup"><span data-stu-id="17961-147">System.String</span></span>
### <span data-ttu-id="17961-148">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="17961-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="17961-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17961-149">OUTPUTS</span></span>

### <span data-ttu-id="17961-150">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="17961-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="17961-151">Note</span><span class="sxs-lookup"><span data-stu-id="17961-151">NOTES</span></span>

## <span data-ttu-id="17961-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17961-152">RELATED LINKS</span></span>

