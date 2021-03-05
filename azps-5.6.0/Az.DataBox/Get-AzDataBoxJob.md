---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: af406af487e03c429a21a99799083f67d0fabf53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998114"
---
# <span data-ttu-id="3150f-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="3150f-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="3150f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3150f-102">SYNOPSIS</span></span>
<span data-ttu-id="3150f-103">Ottiene informazioni sui processi di Databox</span><span class="sxs-lookup"><span data-stu-id="3150f-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="3150f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3150f-104">SYNTAX</span></span>

### <span data-ttu-id="3150f-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3150f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3150f-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150f-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3150f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3150f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3150f-108">DESCRIPTION</span></span>
<span data-ttu-id="3150f-109">Il cmdlet **Get-AzDataBoxJobs** ottiene informazioni sui processi della finestra di dati in una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3150f-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="3150f-110">Se si specifica il gruppo di risorse, questo cmdlet ottiene tutti i processi della casella dei dati in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3150f-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="3150f-111">Se si specifica il nome del processo insieme al nome del gruppo di risorse, questo cmdlet ottiene informazioni sul processo specifico della casella dei dati.</span><span class="sxs-lookup"><span data-stu-id="3150f-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="3150f-112">Se non si specifica altro che l'ID sottoscrizione, questo cmdlet ottiene informazioni su tutti i processi della casella di dati nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3150f-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="3150f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3150f-113">EXAMPLES</span></span>

### <span data-ttu-id="3150f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3150f-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="3150f-115">Get-AzDataBoxJob nessun parametro recupera tutti i processi della casella di dati nella sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3150f-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="3150f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3150f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="3150f-117">Get-AzDataBoxJob con il parametro ResourceGroupName recupera tutti i processi della casella dei dati nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="3150f-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="3150f-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3150f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="3150f-119">Get-AzDataBoxJob con ResourceGroupName e Name specificati recupereranno lo specifico processo della casella di dati</span><span class="sxs-lookup"><span data-stu-id="3150f-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="3150f-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3150f-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="3150f-121">Get-AzDataBoxJob con ResourceId specificato recupererà lo specifico processo della casella dei dati</span><span class="sxs-lookup"><span data-stu-id="3150f-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="3150f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3150f-122">PARAMETERS</span></span>

### <span data-ttu-id="3150f-123">-Interrotto</span><span class="sxs-lookup"><span data-stu-id="3150f-123">-Aborted</span></span>
<span data-ttu-id="3150f-124">Parametro switch per recuperare i processi interrotti</span><span class="sxs-lookup"><span data-stu-id="3150f-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-125">-Annullato</span><span class="sxs-lookup"><span data-stu-id="3150f-125">-Cancelled</span></span>
<span data-ttu-id="3150f-126">Parametro switch per recuperare processi annullati</span><span class="sxs-lookup"><span data-stu-id="3150f-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-127">-Completed</span><span class="sxs-lookup"><span data-stu-id="3150f-127">-Completed</span></span>
<span data-ttu-id="3150f-128">Parametro Switch per recuperare i processi completati</span><span class="sxs-lookup"><span data-stu-id="3150f-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="3150f-129">-CompletedWithError</span></span>
<span data-ttu-id="3150f-130">Parametro switch per recuperare i processi completati con errori</span><span class="sxs-lookup"><span data-stu-id="3150f-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3150f-131">-DefaultProfile</span></span>
<span data-ttu-id="3150f-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3150f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3150f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="3150f-133">-Name</span></span>
<span data-ttu-id="3150f-134">Nome processo casella di dati</span><span class="sxs-lookup"><span data-stu-id="3150f-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3150f-135">-ResourceGroupName</span></span>
<span data-ttu-id="3150f-136">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="3150f-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3150f-137">-ResourceId</span></span>
<span data-ttu-id="3150f-138">ID risorsa processo casella dati</span><span class="sxs-lookup"><span data-stu-id="3150f-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3150f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3150f-139">CommonParameters</span></span>
<span data-ttu-id="3150f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3150f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3150f-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3150f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3150f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3150f-142">INPUTS</span></span>

### <span data-ttu-id="3150f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3150f-143">System.String</span></span>

## <span data-ttu-id="3150f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3150f-144">OUTPUTS</span></span>

### <span data-ttu-id="3150f-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="3150f-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="3150f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3150f-146">NOTES</span></span>

## <span data-ttu-id="3150f-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3150f-147">RELATED LINKS</span></span>
