---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200510"
---
# <span data-ttu-id="2c1ed-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="2c1ed-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="2c1ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ed-103">Ottenere un msixpackage.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-103">Get a msixpackage.</span></span>

## <span data-ttu-id="2c1ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c1ed-104">SYNTAX</span></span>

### <span data-ttu-id="2c1ed-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c1ed-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c1ed-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="2c1ed-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c1ed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c1ed-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c1ed-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2c1ed-108">DESCRIPTION</span></span>
<span data-ttu-id="2c1ed-109">Ottenere un msixpackage.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-109">Get a msixpackage.</span></span>

## <span data-ttu-id="2c1ed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c1ed-110">EXAMPLES</span></span>

### <span data-ttu-id="2c1ed-111">Esempio 1: Ottenere un pacchetto MSIX in base al nome</span><span class="sxs-lookup"><span data-stu-id="2c1ed-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="2c1ed-112">Questo comando ottiene un pacchetto MSIX in un hostPool.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="2c1ed-113">Esempio 2: Elencare i pacchetti MSIX</span><span class="sxs-lookup"><span data-stu-id="2c1ed-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="2c1ed-114">Questo comando elenca i pacchetti MSIX in un hostpool.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="2c1ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c1ed-115">PARAMETERS</span></span>

### <span data-ttu-id="2c1ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ed-116">-DefaultProfile</span></span>
<span data-ttu-id="2c1ed-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1ed-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="2c1ed-118">-FullName</span></span>
<span data-ttu-id="2c1ed-119">Nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c1ed-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2c1ed-120">-HostPoolName</span></span>
<span data-ttu-id="2c1ed-121">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="2c1ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c1ed-122">-InputObject</span></span>
<span data-ttu-id="2c1ed-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c1ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c1ed-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-125">The name of the resource group.</span></span>
<span data-ttu-id="2c1ed-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2c1ed-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c1ed-127">-SubscriptionId</span></span>
<span data-ttu-id="2c1ed-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2c1ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ed-129">CommonParameters</span></span>
<span data-ttu-id="2c1ed-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1ed-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ed-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2c1ed-132">INPUTS</span></span>

### <span data-ttu-id="2c1ed-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2c1ed-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2c1ed-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c1ed-134">OUTPUTS</span></span>

### <span data-ttu-id="2c1ed-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="2c1ed-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="2c1ed-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2c1ed-136">NOTES</span></span>

<span data-ttu-id="2c1ed-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2c1ed-137">ALIASES</span></span>

<span data-ttu-id="2c1ed-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2c1ed-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c1ed-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c1ed-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c1ed-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2c1ed-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c1ed-142">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="2c1ed-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2c1ed-143">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2c1ed-144">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2c1ed-145">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2c1ed-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2c1ed-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c1ed-147">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2c1ed-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2c1ed-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="2c1ed-150">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2c1ed-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c1ed-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2c1ed-152">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="2c1ed-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2c1ed-153">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="2c1ed-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2c1ed-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c1ed-154">RELATED LINKS</span></span>

