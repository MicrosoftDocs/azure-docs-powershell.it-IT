---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 1a5cfb9f9bc7edb436d37847fc117565c3b71221
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023281"
---
# <span data-ttu-id="553f9-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="553f9-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="553f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="553f9-102">SYNOPSIS</span></span>
<span data-ttu-id="553f9-103">Ottieni un'istanza di Update Run usando l'ID.</span><span class="sxs-lookup"><span data-stu-id="553f9-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="553f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="553f9-104">SYNTAX</span></span>

### <span data-ttu-id="553f9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="553f9-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="553f9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="553f9-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="553f9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="553f9-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="553f9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553f9-108">DESCRIPTION</span></span>
<span data-ttu-id="553f9-109">Ottieni un'istanza di Update Run usando l'ID.</span><span class="sxs-lookup"><span data-stu-id="553f9-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="553f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="553f9-110">EXAMPLES</span></span>

### <span data-ttu-id="553f9-111">Esempio 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="553f9-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="553f9-112">Se non viene specificato un valore UpdateName, Get-UpdateRun richiederà sempre l'input.</span><span class="sxs-lookup"><span data-stu-id="553f9-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="553f9-113">Una volta forniti, emetterà tutte le istanze di UpdateRun non riuscite o di successo</span><span class="sxs-lookup"><span data-stu-id="553f9-113">Once provided, it will output all instances of UpdateRun that were Failed or Successfull</span></span>

### <span data-ttu-id="553f9-114">Esempio 2: Get-AzsUpdateRun di UpdateName</span><span class="sxs-lookup"><span data-stu-id="553f9-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="553f9-115">Recupererà tutti i UpdateRuns associati a un aggiornamento specifico</span><span class="sxs-lookup"><span data-stu-id="553f9-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="553f9-116">Esempio 2: Get-AzsUpdateRun per nome</span><span class="sxs-lookup"><span data-stu-id="553f9-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="553f9-117">Recupererà tutti i UpdateRuns associati a un aggiornamento specifico e a un nome specifico</span><span class="sxs-lookup"><span data-stu-id="553f9-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="553f9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="553f9-118">PARAMETERS</span></span>

### <span data-ttu-id="553f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553f9-119">-DefaultProfile</span></span>
<span data-ttu-id="553f9-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="553f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="553f9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="553f9-121">-InputObject</span></span>
<span data-ttu-id="553f9-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="553f9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="553f9-123">-Location</span></span>
<span data-ttu-id="553f9-124">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="553f9-125">-Name</span></span>
<span data-ttu-id="553f9-126">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-126">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="553f9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="553f9-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="553f9-129">-SubscriptionId</span></span>
<span data-ttu-id="553f9-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="553f9-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="553f9-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="553f9-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="553f9-132">-UpdateName</span></span>
<span data-ttu-id="553f9-133">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-133">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="553f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553f9-134">CommonParameters</span></span>
<span data-ttu-id="553f9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553f9-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="553f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553f9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="553f9-137">INPUTS</span></span>

### <span data-ttu-id="553f9-138">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="553f9-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="553f9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="553f9-139">OUTPUTS</span></span>

### <span data-ttu-id="553f9-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="553f9-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="553f9-141">Note</span><span class="sxs-lookup"><span data-stu-id="553f9-141">NOTES</span></span>

<span data-ttu-id="553f9-142">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="553f9-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="553f9-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="553f9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="553f9-144">INPUTOBJECT <IUpdateAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="553f9-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="553f9-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="553f9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="553f9-146">`[ResourceGroupName <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="553f9-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="553f9-147">`[RunName <String>]`: Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="553f9-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="553f9-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="553f9-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="553f9-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="553f9-150">`[UpdateLocation <String>]`: Nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="553f9-151">`[UpdateName <String>]`: Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="553f9-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="553f9-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="553f9-152">RELATED LINKS</span></span>

