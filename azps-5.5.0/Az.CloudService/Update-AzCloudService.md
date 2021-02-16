---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177807"
---
# <span data-ttu-id="af566-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="af566-101">Update-AzCloudService</span></span>

## <span data-ttu-id="af566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af566-102">SYNOPSIS</span></span>
<span data-ttu-id="af566-103">Creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-103">Create or update a cloud service.</span></span>
<span data-ttu-id="af566-104">Tenere presente che alcune proprietà possono essere impostate solo durante la creazione di servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="af566-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af566-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af566-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af566-106">DESCRIPTION</span></span>
<span data-ttu-id="af566-107">Creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-107">Create or update a cloud service.</span></span>
<span data-ttu-id="af566-108">Tenere presente che alcune proprietà possono essere impostate solo durante la creazione di servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="af566-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af566-109">EXAMPLES</span></span>

### <span data-ttu-id="af566-110">Esempio 1: Aggiungere l'estensione RDP a un servizio cloud esistente</span><span class="sxs-lookup"><span data-stu-id="af566-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="af566-111">Il set di comandi precedente aggiunge un'estensione RDP a un servizio cloud già esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="af566-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="af566-112">Esempio 2: Rimuovere tutte le estensioni dal servizio cloud</span><span class="sxs-lookup"><span data-stu-id="af566-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="af566-113">Sopra il set di comandi vengono rimosse tutte le estensioni dal servizio cloud esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="af566-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="af566-114">Esempio 3: Rimuovere l'estensione RDP dal servizio cloud</span><span class="sxs-lookup"><span data-stu-id="af566-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="af566-115">L'insieme di comandi precedente rimuove l'estensione RDP dal servizio cloud esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="af566-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="af566-116">Esempio 4: istanze Scale-Out/Scale-In ruoli</span><span class="sxs-lookup"><span data-stu-id="af566-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="af566-117">Sopra il set di comandi mostra come eseguire la scalabilità orizzontale e il numero di istanze del ruolo di scalabilità per il servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="af566-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="af566-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af566-118">PARAMETERS</span></span>

### <span data-ttu-id="af566-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af566-119">-AsJob</span></span>
<span data-ttu-id="af566-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="af566-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af566-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af566-121">-DefaultProfile</span></span>
<span data-ttu-id="af566-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af566-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af566-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af566-123">-InputObject</span></span>
<span data-ttu-id="af566-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="af566-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af566-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af566-125">-NoWait</span></span>
<span data-ttu-id="af566-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="af566-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af566-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="af566-127">-Parameter</span></span>
<span data-ttu-id="af566-128">Descrive il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-128">Describes the cloud service.</span></span>
<span data-ttu-id="af566-129">Per creare, vedere la sezione NOTE per le proprietà PARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="af566-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af566-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af566-130">-Confirm</span></span>
<span data-ttu-id="af566-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af566-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af566-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af566-132">-WhatIf</span></span>
<span data-ttu-id="af566-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af566-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af566-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af566-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af566-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af566-135">CommonParameters</span></span>
<span data-ttu-id="af566-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af566-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af566-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af566-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af566-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="af566-138">INPUTS</span></span>

### <span data-ttu-id="af566-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="af566-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="af566-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="af566-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="af566-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af566-141">OUTPUTS</span></span>

### <span data-ttu-id="af566-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="af566-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="af566-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="af566-143">NOTES</span></span>

<span data-ttu-id="af566-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af566-144">ALIASES</span></span>

<span data-ttu-id="af566-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="af566-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af566-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="af566-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af566-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af566-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af566-148">INPUTOBJECT <ICloudServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="af566-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af566-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="af566-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="af566-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af566-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="af566-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="af566-152">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="af566-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="af566-153">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="af566-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="af566-154">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="af566-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="af566-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="af566-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="af566-156">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="af566-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="af566-157">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="af566-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="af566-158">PARAMETER: <ICloudService> descrive il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="af566-159">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="af566-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="af566-160">`[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="af566-161">`[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="af566-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="af566-162">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="af566-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="af566-163">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="af566-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="af566-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo di estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="af566-165">`[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="af566-166">`[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può eseguire automaticamente l'aggiornamento di typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="af566-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="af566-167">`[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.</span><span class="sxs-lookup"><span data-stu-id="af566-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="af566-168">La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="af566-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="af566-169">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="af566-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="af566-170">Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno</span><span class="sxs-lookup"><span data-stu-id="af566-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="af566-171">`[Name <String>]`: nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="af566-172">`[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="af566-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="af566-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="af566-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="af566-174">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="af566-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="af566-175">`[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per applicare questa estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="af566-176">Se non si specifica la proprietà o si specifica "\*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="af566-177">`[Setting <String>]`: impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="af566-178">Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="af566-179">Per l'estensione XML, ad esempio RDP, si tratta dell'impostazione XML per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="af566-180">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="af566-181">`[Type <String>]`: specifica il tipo dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="af566-182">`[TypeHandlerVersion <String>]`: specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="af566-183">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-183">Specifies the version of the extension.</span></span> <span data-ttu-id="af566-184">Se questo elemento non viene specificato o come valore viene usato un asterisco (\*), viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="af566-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="af566-185">Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata.</span><span class="sxs-lookup"><span data-stu-id="af566-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="af566-186">Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="af566-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="af566-187">Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="af566-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="af566-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="af566-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="af566-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="af566-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="af566-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="af566-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="af566-192">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="af566-193">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="af566-194">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="af566-195">`[Name <String>]`: nome risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="af566-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="af566-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="af566-197">`[Id <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="af566-198">`[OSProfile <ICloudServiceOSProfile>]`: descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="af566-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="af566-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="af566-200">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="af566-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="af566-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault chiave in SourceVault che contengono certificati.</span><span class="sxs-lookup"><span data-stu-id="af566-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="af566-202">`[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="af566-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="af566-203">`[PackageUrl <String>]`: specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="af566-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="af566-204">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="af566-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="af566-205">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="af566-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="af566-206">`[RoleProfile <ICloudServiceRoleProfile>]`: descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="af566-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="af566-208">`[Name <String>]`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="af566-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="af566-209">`[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="af566-210">`[SkuName <String>]`: il nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="af566-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="af566-211">NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in esecuzione il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.</span><span class="sxs-lookup"><span data-stu-id="af566-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="af566-212">`[SkuTier <String>]`: specifica il livello del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="af566-213">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="af566-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="af566-214">**Standard**</span><span class="sxs-lookup"><span data-stu-id="af566-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="af566-215">**Di base**</span><span class="sxs-lookup"><span data-stu-id="af566-215">**Basic**</span></span>
  - <span data-ttu-id="af566-216">`[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud subito dopo la sua creazione.</span><span class="sxs-lookup"><span data-stu-id="af566-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="af566-217">Il valore predefinito è `true` .</span><span class="sxs-lookup"><span data-stu-id="af566-217">The default value is `true`.</span></span>         <span data-ttu-id="af566-218">Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="af566-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="af566-219">Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio.</span><span class="sxs-lookup"><span data-stu-id="af566-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="af566-220">Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.</span><span class="sxs-lookup"><span data-stu-id="af566-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="af566-221">`[Tag <ICloudServiceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="af566-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="af566-222">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af566-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="af566-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="af566-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="af566-224">Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="af566-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="af566-225">Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="af566-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="af566-226">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="af566-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="af566-227">**Automatico**</span><span class="sxs-lookup"><span data-stu-id="af566-227">**Auto**</span></span><br /><br /><span data-ttu-id="af566-228">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="af566-228">**Manual**</span></span> <br /><br /><span data-ttu-id="af566-229">**Simultaneo**</span><span class="sxs-lookup"><span data-stu-id="af566-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="af566-230">Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="af566-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="af566-231">Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="af566-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="af566-232">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af566-232">RELATED LINKS</span></span>

