---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 5594e43b2e6c67e9df5b526f753557edd8a4d5ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414731"
---
# <span data-ttu-id="e3538-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-101">Set-AzWebApp</span></span>

## <span data-ttu-id="e3538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3538-102">SYNOPSIS</span></span>
<span data-ttu-id="e3538-103">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="e3538-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3538-104">SYNTAX</span></span>

### <span data-ttu-id="e3538-105">S1</span><span class="sxs-lookup"><span data-stu-id="e3538-105">S1</span></span>
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

### <span data-ttu-id="e3538-106">S2</span><span class="sxs-lookup"><span data-stu-id="e3538-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3538-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3538-107">DESCRIPTION</span></span>
<span data-ttu-id="e3538-108">Il cmdlet **Set-AzWebApp** imposta un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="e3538-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3538-109">EXAMPLES</span></span>

### <span data-ttu-id="e3538-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3538-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="e3538-111">Questo comando modifica il piano di servizio app associato all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e3538-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e3538-112">Usare il collegamento per altre informazioni su come modificare il piano di servizio app e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="e3538-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="e3538-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="e3538-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="e3538-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e3538-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="e3538-115">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="e3538-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="e3538-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e3538-116">Example 3</span></span>

<span data-ttu-id="e3538-117">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="e3538-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="e3538-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="e3538-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e3538-119">Example 4</span></span>

<span data-ttu-id="e3538-120">L'esempio seguente crea una stringa di connessione denominata myConnectionString per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="e3538-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="e3538-121">Verranno sostituite tutte le stringhe di connessione esistenti per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="e3538-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="e3538-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3538-122">PARAMETERS</span></span>

### <span data-ttu-id="e3538-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="e3538-123">-AlwaysOn</span></span>
<span data-ttu-id="e3538-124">Assicurarsi che l'app Web venga caricata di tanto in tanto, piuttosto che dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="e3538-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="e3538-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e3538-125">-AppServicePlan</span></span>
<span data-ttu-id="e3538-126">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="e3538-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="e3538-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e3538-127">-AppSettings</span></span>
<span data-ttu-id="e3538-128">Tabella HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="e3538-128">App Settings HashTable.</span></span> <span data-ttu-id="e3538-129">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo quelle non disponibili.</span><span class="sxs-lookup"><span data-stu-id="e3538-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="e3538-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3538-130">-AsJob</span></span>
<span data-ttu-id="e3538-131">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3538-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3538-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e3538-132">-AssignIdentity</span></span>
<span data-ttu-id="e3538-133">Abilitare/disabilitare MSI in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="e3538-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e3538-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e3538-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="e3538-135">Nome slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="e3538-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="e3538-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="e3538-136">-AzureStoragePath</span></span>
<span data-ttu-id="e3538-137">Archiviazione di Azure per il montaggio all'interno di un'app Web per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3538-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="e3538-138">Usare New-AzureRmWebAppAzureStoragePath per crearla</span><span class="sxs-lookup"><span data-stu-id="e3538-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="e3538-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e3538-139">-ConnectionStrings</span></span>
<span data-ttu-id="e3538-140">Tabella HashTable delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="e3538-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="e3538-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e3538-141">-ContainerImageName</span></span>
<span data-ttu-id="e3538-142">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="e3538-142">Container Image Name</span></span>

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

### <span data-ttu-id="e3538-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e3538-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e3538-144">Password del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="e3538-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="e3538-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e3538-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e3538-146">Url del server del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="e3538-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="e3538-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e3538-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="e3538-148">Nome utente del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="e3538-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="e3538-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e3538-149">-DefaultDocuments</span></span>
<span data-ttu-id="e3538-150">Matrice di stringhe di documenti predefinite</span><span class="sxs-lookup"><span data-stu-id="e3538-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="e3538-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3538-151">-DefaultProfile</span></span>
<span data-ttu-id="e3538-152">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3538-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3538-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e3538-154">Booleano registrazione errori dettagliato abilitato</span><span class="sxs-lookup"><span data-stu-id="e3538-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="e3538-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e3538-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e3538-156">Webhook di distribuzione continua contenitore/disabilita</span><span class="sxs-lookup"><span data-stu-id="e3538-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="e3538-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="e3538-157">-FtpsState</span></span>
<span data-ttu-id="e3538-158">Impostare il valore dello stato ftp per un'app.</span><span class="sxs-lookup"><span data-stu-id="e3538-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="e3538-159">Valori consentiti [AllAllowed | Disabilitato | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="e3538-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="e3538-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e3538-160">-HandlerMappings</span></span>
<span data-ttu-id="e3538-161">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="e3538-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="e3538-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="e3538-162">-HostNames</span></span>
<span data-ttu-id="e3538-163">Matrice stringa HostNames della WebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="e3538-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3538-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e3538-165">Booleano HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3538-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="e3538-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e3538-166">-HttpsOnly</span></span>
<span data-ttu-id="e3538-167">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="e3538-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e3538-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e3538-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="e3538-169">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="e3538-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="e3538-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e3538-170">-MinTlsVersion</span></span>
<span data-ttu-id="e3538-171">Versione minima di TLS richiesta per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="e3538-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="e3538-172">Valori consentiti [1,0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="e3538-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="e3538-173">-Name</span><span class="sxs-lookup"><span data-stu-id="e3538-173">-Name</span></span>
<span data-ttu-id="e3538-174">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-174">WebApp Name</span></span>

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

### <span data-ttu-id="e3538-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e3538-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="e3538-176">Versione di Net Framework</span><span class="sxs-lookup"><span data-stu-id="e3538-176">Net Framework Version</span></span>

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

### <span data-ttu-id="e3538-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e3538-177">-NumberOfWorkers</span></span>
<span data-ttu-id="e3538-178">Il numero di lavoratori da allocare</span><span class="sxs-lookup"><span data-stu-id="e3538-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="e3538-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e3538-179">-PhpVersion</span></span>
<span data-ttu-id="e3538-180">Versione Php</span><span class="sxs-lookup"><span data-stu-id="e3538-180">Php Version</span></span>

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

### <span data-ttu-id="e3538-181">-RequestTenabled</span><span class="sxs-lookup"><span data-stu-id="e3538-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="e3538-182">Traccia richiesta abilitata</span><span class="sxs-lookup"><span data-stu-id="e3538-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="e3538-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3538-183">-ResourceGroupName</span></span>
<span data-ttu-id="e3538-184">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e3538-184">Resource Group Name</span></span>

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

### <span data-ttu-id="e3538-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e3538-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e3538-186">Usare la funzione booleana Processo di lavoro a 32 bit</span><span class="sxs-lookup"><span data-stu-id="e3538-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="e3538-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-187">-WebApp</span></span>
<span data-ttu-id="e3538-188">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-188">WebApp Object</span></span>

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

### <span data-ttu-id="e3538-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e3538-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="e3538-190">Booleano WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e3538-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="e3538-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3538-191">CommonParameters</span></span>
<span data-ttu-id="e3538-192">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3538-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3538-193">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3538-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3538-194">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3538-194">INPUTS</span></span>

### <span data-ttu-id="e3538-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e3538-195">System.Int32</span></span>

### <span data-ttu-id="e3538-196">System.String</span><span class="sxs-lookup"><span data-stu-id="e3538-196">System.String</span></span>

### <span data-ttu-id="e3538-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e3538-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e3538-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3538-198">OUTPUTS</span></span>

### <span data-ttu-id="e3538-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e3538-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e3538-200">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3538-200">NOTES</span></span>
<span data-ttu-id="e3538-201">Il cmdlet fornito di seguito aiuta ad aggiornare Azure Web App a **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="e3538-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="e3538-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="e3538-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="e3538-203">Sostituire i valori di Default-Web-WestUS con il nome del gruppo di risorse della webapp e di ContosoWebApp con il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="e3538-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="e3538-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3538-204">RELATED LINKS</span></span>

[<span data-ttu-id="e3538-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e3538-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e3538-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e3538-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e3538-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e3538-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3538-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

