---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835267"
---
# <span data-ttu-id="c0563-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="c0563-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="c0563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0563-102">SYNOPSIS</span></span>
<span data-ttu-id="c0563-103">Controlla se sono disponibili aggiornamenti per i servizi di sistema associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="c0563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0563-104">SYNTAX</span></span>

### <span data-ttu-id="c0563-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0563-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0563-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0563-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0563-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0563-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0563-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0563-108">DESCRIPTION</span></span>
<span data-ttu-id="c0563-109">I servizi di sistema ricevono gli aggiornamenti in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="c0563-110">L'uso di questo cmdlet consentirà all'utente di sapere se Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="c0563-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="c0563-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0563-111">EXAMPLES</span></span>

### <span data-ttu-id="c0563-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0563-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="c0563-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c0563-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="c0563-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c0563-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="c0563-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0563-115">PARAMETERS</span></span>

### <span data-ttu-id="c0563-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0563-116">-DefaultProfile</span></span>
<span data-ttu-id="c0563-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0563-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0563-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0563-118">-InputObject</span></span>
<span data-ttu-id="c0563-119">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0563-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0563-120">-Name</span></span>
<span data-ttu-id="c0563-121">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0563-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0563-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0563-123">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0563-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0563-124">-ResourceId</span></span>
<span data-ttu-id="c0563-125">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c0563-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0563-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0563-126">CommonParameters</span></span>
<span data-ttu-id="c0563-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0563-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0563-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0563-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0563-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0563-129">INPUTS</span></span>

### <span data-ttu-id="c0563-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c0563-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="c0563-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c0563-131">System.String</span></span>

## <span data-ttu-id="c0563-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0563-132">OUTPUTS</span></span>

### <span data-ttu-id="c0563-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="c0563-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="c0563-134">Note</span><span class="sxs-lookup"><span data-stu-id="c0563-134">NOTES</span></span>

## <span data-ttu-id="c0563-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0563-135">RELATED LINKS</span></span>
