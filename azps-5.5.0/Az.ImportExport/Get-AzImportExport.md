---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209355"
---
# <span data-ttu-id="8eff2-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8eff2-101">Get-AzImportExport</span></span>

## <span data-ttu-id="8eff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eff2-102">SYNOPSIS</span></span>
<span data-ttu-id="8eff2-103">Ottiene informazioni su un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="8eff2-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="8eff2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eff2-104">SYNTAX</span></span>

### <span data-ttu-id="8eff2-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8eff2-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8eff2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8eff2-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8eff2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8eff2-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8eff2-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="8eff2-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8eff2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8eff2-109">DESCRIPTION</span></span>
<span data-ttu-id="8eff2-110">Ottiene informazioni su un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="8eff2-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="8eff2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eff2-111">EXAMPLES</span></span>

### <span data-ttu-id="8eff2-112">Esempio 1: Ottenere il processo ImportExport con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="8eff2-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8eff2-113">Questo cmdlet ottiene il processo ImportExport con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="8eff2-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="8eff2-114">Esempio 2: Ottenere il processo ImportExport in base al gruppo di risorse e al nome del processo</span><span class="sxs-lookup"><span data-stu-id="8eff2-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8eff2-115">Questo cmdlet ottiene il processo ImportExport in base al gruppo di risorse e al nome del processo.</span><span class="sxs-lookup"><span data-stu-id="8eff2-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="8eff2-116">Esempio 3: Elenco di tutti i processi ImportExport nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8eff2-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8eff2-117">Questo cmdlet elenca tutti i processi ImportExport nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8eff2-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="8eff2-118">Esempio 4: Ottenere il processo ImportExport in base all'identità</span><span class="sxs-lookup"><span data-stu-id="8eff2-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="8eff2-119">Questo elenco di cmdlet ottiene il processo importExport in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="8eff2-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="8eff2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eff2-120">PARAMETERS</span></span>

### <span data-ttu-id="8eff2-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="8eff2-121">-AcceptLanguage</span></span>
<span data-ttu-id="8eff2-122">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="8eff2-122">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eff2-123">-DefaultProfile</span></span>
<span data-ttu-id="8eff2-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8eff2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="8eff2-125">-Filter</span></span>
<span data-ttu-id="8eff2-126">Può essere usato per limitare i risultati a determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="8eff2-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eff2-127">-InputObject</span></span>
<span data-ttu-id="8eff2-128">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8eff2-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8eff2-129">-Name</span></span>
<span data-ttu-id="8eff2-130">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="8eff2-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eff2-131">-ResourceGroupName</span></span>
<span data-ttu-id="8eff2-132">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8eff2-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8eff2-133">-SubscriptionId</span></span>
<span data-ttu-id="8eff2-134">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="8eff2-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-135">-In alto</span><span class="sxs-lookup"><span data-stu-id="8eff2-135">-Top</span></span>
<span data-ttu-id="8eff2-136">Valore intero che specifica il numero massimo di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="8eff2-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="8eff2-137">Il valore non può essere superiore a 100.</span><span class="sxs-lookup"><span data-stu-id="8eff2-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eff2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eff2-138">CommonParameters</span></span>
<span data-ttu-id="8eff2-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eff2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eff2-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8eff2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eff2-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="8eff2-141">INPUTS</span></span>

### <span data-ttu-id="8eff2-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="8eff2-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="8eff2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eff2-143">OUTPUTS</span></span>

### <span data-ttu-id="8eff2-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="8eff2-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="8eff2-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="8eff2-145">NOTES</span></span>

<span data-ttu-id="8eff2-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8eff2-146">ALIASES</span></span>

<span data-ttu-id="8eff2-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8eff2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8eff2-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8eff2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8eff2-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8eff2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8eff2-150">INPUTOBJECT <IImportExportIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="8eff2-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8eff2-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8eff2-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8eff2-152">`[JobName <String>]`: nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="8eff2-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="8eff2-153">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="8eff2-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="8eff2-154">Ad esempio, Stati Uniti occidentali o Ovest.</span><span class="sxs-lookup"><span data-stu-id="8eff2-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="8eff2-155">`[ResourceGroupName <String>]`: il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8eff2-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="8eff2-156">`[SubscriptionId <String>]`: ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="8eff2-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="8eff2-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eff2-157">RELATED LINKS</span></span>

