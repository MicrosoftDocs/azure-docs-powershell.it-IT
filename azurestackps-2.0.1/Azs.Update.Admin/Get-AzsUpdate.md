---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023131"
---
# <span data-ttu-id="5cf6a-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="5cf6a-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="5cf6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf6a-103">Ottenere un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="5cf6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cf6a-104">SYNTAX</span></span>

### <span data-ttu-id="5cf6a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cf6a-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cf6a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5cf6a-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cf6a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf6a-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5cf6a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cf6a-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf6a-109">Ottenere un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="5cf6a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cf6a-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf6a-111">Esempio 1: ottenere tutti gli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="5cf6a-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="5cf6a-112">Senza parametri, Get-AzsUpdate elenca tutti gli aggiornamenti che il timbro può individuare</span><span class="sxs-lookup"><span data-stu-id="5cf6a-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="5cf6a-113">Esempio 2: ottenere l'aggiornamento in base al nome</span><span class="sxs-lookup"><span data-stu-id="5cf6a-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="5cf6a-114">Recupererà tutti gli aggiornamenti che corrispondono al nome specificato</span><span class="sxs-lookup"><span data-stu-id="5cf6a-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="5cf6a-115">Esempio 3: ottenere tutti gli aggiornamenti in base alla posizione</span><span class="sxs-lookup"><span data-stu-id="5cf6a-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="5cf6a-116">Recupererà tutti gli aggiornamenti in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="5cf6a-117">Attualmente è supportata solo una posizione, quindi questo è l'equivalente solo Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="5cf6a-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="5cf6a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cf6a-118">PARAMETERS</span></span>

### <span data-ttu-id="5cf6a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf6a-119">-DefaultProfile</span></span>
<span data-ttu-id="5cf6a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf6a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cf6a-121">-InputObject</span></span>
<span data-ttu-id="5cf6a-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cf6a-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5cf6a-123">-Location</span></span>
<span data-ttu-id="5cf6a-124">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-124">The name of the update location.</span></span>

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

### <span data-ttu-id="5cf6a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cf6a-125">-Name</span></span>
<span data-ttu-id="5cf6a-126">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-126">Name of the update.</span></span>

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

### <span data-ttu-id="5cf6a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf6a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cf6a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-128">Resource group name.</span></span>

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

### <span data-ttu-id="5cf6a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cf6a-129">-SubscriptionId</span></span>
<span data-ttu-id="5cf6a-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5cf6a-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cf6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf6a-132">CommonParameters</span></span>
<span data-ttu-id="5cf6a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf6a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf6a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cf6a-135">INPUTS</span></span>

### <span data-ttu-id="5cf6a-136">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf6a-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="5cf6a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cf6a-137">OUTPUTS</span></span>

### <span data-ttu-id="5cf6a-138">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="5cf6a-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="5cf6a-139">Note</span><span class="sxs-lookup"><span data-stu-id="5cf6a-139">NOTES</span></span>

<span data-ttu-id="5cf6a-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cf6a-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5cf6a-142">INPUTOBJECT <IUpdateAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5cf6a-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cf6a-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5cf6a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cf6a-144">`[ResourceGroupName <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="5cf6a-145">`[RunName <String>]`: Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="5cf6a-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="5cf6a-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5cf6a-148">`[UpdateLocation <String>]`: Nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="5cf6a-149">`[UpdateName <String>]`: Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="5cf6a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cf6a-150">RELATED LINKS</span></span>

