---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387320"
---
# <span data-ttu-id="a703f-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a703f-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="a703f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a703f-102">SYNOPSIS</span></span>
<span data-ttu-id="a703f-103">Ottenere un msixpackage.</span><span class="sxs-lookup"><span data-stu-id="a703f-103">Get a msixpackage.</span></span>

## <span data-ttu-id="a703f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a703f-104">SYNTAX</span></span>

### <span data-ttu-id="a703f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a703f-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a703f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a703f-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a703f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a703f-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a703f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a703f-108">DESCRIPTION</span></span>
<span data-ttu-id="a703f-109">Ottenere un msixpackage.</span><span class="sxs-lookup"><span data-stu-id="a703f-109">Get a msixpackage.</span></span>

## <span data-ttu-id="a703f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a703f-110">EXAMPLES</span></span>

### <span data-ttu-id="a703f-111">Esempio 1: ottenere un pacchetto MSIX in base al nome</span><span class="sxs-lookup"><span data-stu-id="a703f-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a703f-112">Questo comando ottiene un pacchetto MSIX in un HostPool.</span><span class="sxs-lookup"><span data-stu-id="a703f-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="a703f-113">Esempio 2: elenco di pacchetti MSIX</span><span class="sxs-lookup"><span data-stu-id="a703f-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a703f-114">Questo comando elenca i pacchetti MSIX in un HostPool.</span><span class="sxs-lookup"><span data-stu-id="a703f-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="a703f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a703f-115">PARAMETERS</span></span>

### <span data-ttu-id="a703f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a703f-116">-DefaultProfile</span></span>
<span data-ttu-id="a703f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a703f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a703f-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="a703f-118">-FullName</span></span>
<span data-ttu-id="a703f-119">Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="a703f-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a703f-120">-HostPoolName</span></span>
<span data-ttu-id="a703f-121">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a703f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a703f-122">-InputObject</span></span>
<span data-ttu-id="a703f-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a703f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a703f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a703f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a703f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a703f-125">The name of the resource group.</span></span>
<span data-ttu-id="a703f-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a703f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a703f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a703f-127">-SubscriptionId</span></span>
<span data-ttu-id="a703f-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a703f-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a703f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a703f-129">CommonParameters</span></span>
<span data-ttu-id="a703f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a703f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a703f-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a703f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a703f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a703f-132">INPUTS</span></span>

### <span data-ttu-id="a703f-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a703f-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a703f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a703f-134">OUTPUTS</span></span>

### <span data-ttu-id="a703f-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a703f-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="a703f-136">Note</span><span class="sxs-lookup"><span data-stu-id="a703f-136">NOTES</span></span>

<span data-ttu-id="a703f-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a703f-137">ALIASES</span></span>

<span data-ttu-id="a703f-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a703f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a703f-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a703f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a703f-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a703f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a703f-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a703f-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a703f-142">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="a703f-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a703f-143">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a703f-144">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a703f-145">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a703f-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a703f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a703f-147">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a703f-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a703f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a703f-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a703f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a703f-150">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a703f-151">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a703f-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a703f-152">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="a703f-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a703f-153">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="a703f-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a703f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a703f-154">RELATED LINKS</span></span>

