---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474714"
---
# <span data-ttu-id="ed423-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-101">Set-AzWebApp</span></span>

## <span data-ttu-id="ed423-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed423-102">SYNOPSIS</span></span>
<span data-ttu-id="ed423-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="ed423-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="ed423-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed423-104">SYNTAX</span></span>

### <span data-ttu-id="ed423-105">S1</span><span class="sxs-lookup"><span data-stu-id="ed423-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed423-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed423-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed423-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed423-107">DESCRIPTION</span></span>
<span data-ttu-id="ed423-108">Il cmdlet **set-AzWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ed423-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ed423-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed423-109">EXAMPLES</span></span>

### <span data-ttu-id="ed423-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed423-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="ed423-111">Questo comando modifica il piano Appservice associato all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ed423-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ed423-112">Usare il collegamento per altre informazioni su come modificare il piano Appservice e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="ed423-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="ed423-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="ed423-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="ed423-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ed423-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ed423-115">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ed423-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="ed423-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ed423-116">Example 3</span></span>

<span data-ttu-id="ed423-117">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="ed423-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="ed423-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ed423-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="ed423-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ed423-119">Example 4</span></span>

<span data-ttu-id="ed423-120">Nell'esempio seguente viene creata una stringa di connessione denominata ConnectionString per Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ed423-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="ed423-121">Questo sostituisce tutte le stringhe di connessione esistenti per ContosoWebApp Web App.</span><span class="sxs-lookup"><span data-stu-id="ed423-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="ed423-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed423-122">PARAMETERS</span></span>

### <span data-ttu-id="ed423-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="ed423-123">-AlwaysOn</span></span>
<span data-ttu-id="ed423-124">Assicurarsi che l'app Web venga caricata per sempre, invece scaricata dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="ed423-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed423-125">-AppServicePlan</span></span>
<span data-ttu-id="ed423-126">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ed423-126">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ed423-127">-AppSettings</span></span>
<span data-ttu-id="ed423-128">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="ed423-128">App Settings HashTable.</span></span> <span data-ttu-id="ed423-129">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo tutte le impostazioni non fornite.</span><span class="sxs-lookup"><span data-stu-id="ed423-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed423-130">-AsJob</span></span>
<span data-ttu-id="ed423-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed423-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed423-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ed423-132">-AssignIdentity</span></span>
<span data-ttu-id="ed423-133">Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="ed423-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ed423-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="ed423-135">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="ed423-135">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ed423-136">-AzureStoragePath</span></span>
<span data-ttu-id="ed423-137">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="ed423-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="ed423-138">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="ed423-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ed423-139">-ConnectionStrings</span></span>
<span data-ttu-id="ed423-140">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="ed423-140">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ed423-141">-ContainerImageName</span></span>
<span data-ttu-id="ed423-142">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="ed423-142">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ed423-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ed423-144">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ed423-144">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ed423-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ed423-146">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ed423-146">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ed423-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="ed423-148">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ed423-148">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ed423-149">-DefaultDocuments</span></span>
<span data-ttu-id="ed423-150">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="ed423-150">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed423-151">-DefaultProfile</span></span>
<span data-ttu-id="ed423-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed423-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed423-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed423-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ed423-154">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="ed423-154">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ed423-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ed423-156">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="ed423-156">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="ed423-157">-FtpsState</span></span>
<span data-ttu-id="ed423-158">Imposta il valore di stato FTPS per un'app.</span><span class="sxs-lookup"><span data-stu-id="ed423-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="ed423-159">Valori consentiti [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="ed423-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ed423-160">-HandlerMappings</span></span>
<span data-ttu-id="ed423-161">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="ed423-161">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-162">-HostName</span><span class="sxs-lookup"><span data-stu-id="ed423-162">-HostNames</span></span>
<span data-ttu-id="ed423-163">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="ed423-163">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed423-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ed423-165">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ed423-165">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ed423-166">-HttpsOnly</span></span>
<span data-ttu-id="ed423-167">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente</span><span class="sxs-lookup"><span data-stu-id="ed423-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ed423-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="ed423-169">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="ed423-169">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ed423-170">-MinTlsVersion</span></span>
<span data-ttu-id="ed423-171">La versione minima di TLS necessaria per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="ed423-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="ed423-172">Valori consentiti [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="ed423-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-173">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed423-173">-Name</span></span>
<span data-ttu-id="ed423-174">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ed423-174">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ed423-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="ed423-176">NET Framework</span><span class="sxs-lookup"><span data-stu-id="ed423-176">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ed423-177">-NumberOfWorkers</span></span>
<span data-ttu-id="ed423-178">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="ed423-178">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ed423-179">-PhpVersion</span></span>
<span data-ttu-id="ed423-180">Versione php</span><span class="sxs-lookup"><span data-stu-id="ed423-180">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed423-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="ed423-182">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="ed423-182">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed423-183">-ResourceGroupName</span></span>
<span data-ttu-id="ed423-184">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ed423-184">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ed423-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ed423-186">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="ed423-186">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-187">-Web App</span><span class="sxs-lookup"><span data-stu-id="ed423-187">-WebApp</span></span>
<span data-ttu-id="ed423-188">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ed423-188">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ed423-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="ed423-190">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ed423-190">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed423-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed423-191">CommonParameters</span></span>
<span data-ttu-id="ed423-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed423-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed423-193">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed423-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed423-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed423-194">INPUTS</span></span>

### <span data-ttu-id="ed423-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ed423-195">System.Int32</span></span>

### <span data-ttu-id="ed423-196">System. String</span><span class="sxs-lookup"><span data-stu-id="ed423-196">System.String</span></span>

### <span data-ttu-id="ed423-197">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ed423-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed423-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed423-198">OUTPUTS</span></span>

### <span data-ttu-id="ed423-199">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ed423-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed423-200">Note</span><span class="sxs-lookup"><span data-stu-id="ed423-200">NOTES</span></span>
<span data-ttu-id="ed423-201">Il cmdlet seguente consente di aggiornare Azure Web App in **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="ed423-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="ed423-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "default-Web-Westus"-ResourceType Microsoft. Web/sites/config-resourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="ed423-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="ed423-203">Sostituisci i valori di default-Web-Westus con il nome del gruppo di risorse Web App e ContosoWebApp con il nome di Web App.</span><span class="sxs-lookup"><span data-stu-id="ed423-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="ed423-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed423-204">RELATED LINKS</span></span>

[<span data-ttu-id="ed423-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ed423-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ed423-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ed423-208">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ed423-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ed423-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ed423-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="ed423-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed423-211">New-AzResource</span></span>](./New-AzResource.md)
