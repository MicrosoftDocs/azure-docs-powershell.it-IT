---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190705"
---
# <span data-ttu-id="987e1-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="987e1-101">Get-AzImportExport</span></span>

## <span data-ttu-id="987e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="987e1-102">SYNOPSIS</span></span>
<span data-ttu-id="987e1-103">Ottiene informazioni su un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="987e1-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="987e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="987e1-104">SYNTAX</span></span>

### <span data-ttu-id="987e1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="987e1-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="987e1-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="987e1-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="987e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="987e1-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="987e1-108">List1</span><span class="sxs-lookup"><span data-stu-id="987e1-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="987e1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="987e1-109">DESCRIPTION</span></span>
<span data-ttu-id="987e1-110">Ottiene informazioni su un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="987e1-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="987e1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="987e1-111">EXAMPLES</span></span>

### <span data-ttu-id="987e1-112">Esempio 1: ottenere un processo ImportExport con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="987e1-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="987e1-113">Questo cmdlet ottiene il processo ImportExport con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="987e1-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="987e1-114">Esempio 2: ottenere un processo di ImportExport per gruppo di risorse e nome processo</span><span class="sxs-lookup"><span data-stu-id="987e1-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="987e1-115">Questo cmdlet ottiene il processo ImportExport in base al gruppo di risorse e al nome del processo.</span><span class="sxs-lookup"><span data-stu-id="987e1-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="987e1-116">Esempio 3: elenca tutti i processi di ImportExport nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="987e1-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="987e1-117">Questo cmdlet elenca tutti i processi di ImportExport nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="987e1-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="987e1-118">Esempio 4: ottenere un processo di ImportExport per identità</span><span class="sxs-lookup"><span data-stu-id="987e1-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="987e1-119">Questo cmdlet elenca ottiene il processo ImportExport per identità.</span><span class="sxs-lookup"><span data-stu-id="987e1-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="987e1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="987e1-120">PARAMETERS</span></span>

### <span data-ttu-id="987e1-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="987e1-121">-AcceptLanguage</span></span>
<span data-ttu-id="987e1-122">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="987e1-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="987e1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987e1-123">-DefaultProfile</span></span>
<span data-ttu-id="987e1-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="987e1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987e1-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="987e1-125">-Filter</span></span>
<span data-ttu-id="987e1-126">Può essere usato per limitare i risultati a determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="987e1-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="987e1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="987e1-127">-InputObject</span></span>
<span data-ttu-id="987e1-128">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="987e1-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="987e1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="987e1-129">-Name</span></span>
<span data-ttu-id="987e1-130">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="987e1-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="987e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="987e1-132">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="987e1-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="987e1-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="987e1-133">-SubscriptionId</span></span>
<span data-ttu-id="987e1-134">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="987e1-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="987e1-135">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="987e1-135">-Top</span></span>
<span data-ttu-id="987e1-136">Valore integer che specifica il numero di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="987e1-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="987e1-137">Il valore non può superare 100.</span><span class="sxs-lookup"><span data-stu-id="987e1-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="987e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987e1-138">CommonParameters</span></span>
<span data-ttu-id="987e1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987e1-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="987e1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987e1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="987e1-141">INPUTS</span></span>

### <span data-ttu-id="987e1-142">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="987e1-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="987e1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="987e1-143">OUTPUTS</span></span>

### <span data-ttu-id="987e1-144">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="987e1-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="987e1-145">Note</span><span class="sxs-lookup"><span data-stu-id="987e1-145">NOTES</span></span>

<span data-ttu-id="987e1-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="987e1-146">ALIASES</span></span>

<span data-ttu-id="987e1-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="987e1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="987e1-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="987e1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="987e1-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="987e1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="987e1-150">INPUTOBJECT <IImportExportIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="987e1-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="987e1-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="987e1-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="987e1-152">`[JobName <String>]`: Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="987e1-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="987e1-153">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="987e1-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="987e1-154">Ad esempio, ovest degli Stati Uniti o westus.</span><span class="sxs-lookup"><span data-stu-id="987e1-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="987e1-155">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="987e1-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="987e1-156">`[SubscriptionId <String>]`: ID abbonamento per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="987e1-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="987e1-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="987e1-157">RELATED LINKS</span></span>
