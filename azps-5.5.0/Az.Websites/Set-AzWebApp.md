---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197230"
---
# <span data-ttu-id="ddb6e-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-101">Set-AzWebApp</span></span>

## <span data-ttu-id="ddb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb6e-103">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="ddb6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddb6e-104">SYNTAX</span></span>

### <span data-ttu-id="ddb6e-105">S1</span><span class="sxs-lookup"><span data-stu-id="ddb6e-105">S1</span></span>
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

### <span data-ttu-id="ddb6e-106">S2</span><span class="sxs-lookup"><span data-stu-id="ddb6e-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb6e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddb6e-107">DESCRIPTION</span></span>
<span data-ttu-id="ddb6e-108">Il cmdlet **Set-AzWebApp** imposta un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ddb6e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddb6e-109">EXAMPLES</span></span>

### <span data-ttu-id="ddb6e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddb6e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="ddb6e-111">Questo comando modifica il piano di servizio app associato all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ddb6e-112">Usare il collegamento per altre informazioni su come modificare il piano di servizio app e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="ddb6e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="ddb6e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="ddb6e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ddb6e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ddb6e-115">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="ddb6e-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="ddb6e-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ddb6e-116">Example 3</span></span>

<span data-ttu-id="ddb6e-117">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="ddb6e-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="ddb6e-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="ddb6e-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ddb6e-119">Example 4</span></span>

<span data-ttu-id="ddb6e-120">L'esempio seguente crea una stringa di connessione denominata myConnectionString per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="ddb6e-121">Verranno sostituite tutte le stringhe di connessione esistenti per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="ddb6e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb6e-122">PARAMETERS</span></span>

### <span data-ttu-id="ddb6e-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="ddb6e-123">-AlwaysOn</span></span>
<span data-ttu-id="ddb6e-124">Assicurarsi che l'app Web venga caricata di tanto in tanto, piuttosto che dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="ddb6e-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ddb6e-125">-AppServicePlan</span></span>
<span data-ttu-id="ddb6e-126">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="ddb6e-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="ddb6e-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ddb6e-127">-AppSettings</span></span>
<span data-ttu-id="ddb6e-128">Tabella HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-128">App Settings HashTable.</span></span> <span data-ttu-id="ddb6e-129">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo quelle non disponibili.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="ddb6e-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddb6e-130">-AsJob</span></span>
<span data-ttu-id="ddb6e-131">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ddb6e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddb6e-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ddb6e-132">-AssignIdentity</span></span>
<span data-ttu-id="ddb6e-133">Abilitare/disabilitare MSI in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="ddb6e-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="ddb6e-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ddb6e-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="ddb6e-135">Nome slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="ddb6e-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="ddb6e-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ddb6e-136">-AzureStoragePath</span></span>
<span data-ttu-id="ddb6e-137">Archiviazione di Azure per il montaggio all'interno di un'app Web per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="ddb6e-138">Usare New-AzureRmWebAppAzureStoragePath per crearla</span><span class="sxs-lookup"><span data-stu-id="ddb6e-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="ddb6e-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ddb6e-139">-ConnectionStrings</span></span>
<span data-ttu-id="ddb6e-140">Tabella HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="ddb6e-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="ddb6e-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ddb6e-141">-ContainerImageName</span></span>
<span data-ttu-id="ddb6e-142">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="ddb6e-142">Container Image Name</span></span>

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

### <span data-ttu-id="ddb6e-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ddb6e-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ddb6e-144">Password del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ddb6e-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="ddb6e-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ddb6e-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ddb6e-146">Url del server del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ddb6e-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="ddb6e-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ddb6e-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="ddb6e-148">Nome utente del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ddb6e-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="ddb6e-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ddb6e-149">-DefaultDocuments</span></span>
<span data-ttu-id="ddb6e-150">Matrice stringa documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="ddb6e-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="ddb6e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb6e-151">-DefaultProfile</span></span>
<span data-ttu-id="ddb6e-152">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb6e-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ddb6e-154">Booleano di registrazione degli errori dettagliato abilitato</span><span class="sxs-lookup"><span data-stu-id="ddb6e-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="ddb6e-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ddb6e-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ddb6e-156">Abilita/disabilita il webhook della distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="ddb6e-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ddb6e-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="ddb6e-157">-FtpsState</span></span>
<span data-ttu-id="ddb6e-158">Impostare il valore dello stato ftp per un'app.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="ddb6e-159">Valori consentiti [AllAllowed | Disabilitato | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="ddb6e-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="ddb6e-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ddb6e-160">-HandlerMappings</span></span>
<span data-ttu-id="ddb6e-161">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="ddb6e-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="ddb6e-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="ddb6e-162">-HostNames</span></span>
<span data-ttu-id="ddb6e-163">Matrice stringa HostNames della WebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="ddb6e-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ddb6e-165">Booleano HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="ddb6e-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ddb6e-166">-HttpsOnly</span></span>
<span data-ttu-id="ddb6e-167">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="ddb6e-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="ddb6e-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ddb6e-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="ddb6e-169">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="ddb6e-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="ddb6e-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ddb6e-170">-MinTlsVersion</span></span>
<span data-ttu-id="ddb6e-171">La versione minima di TLS richiesta per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="ddb6e-172">Valori consentiti [1,0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="ddb6e-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="ddb6e-173">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb6e-173">-Name</span></span>
<span data-ttu-id="ddb6e-174">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-174">WebApp Name</span></span>

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

### <span data-ttu-id="ddb6e-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ddb6e-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="ddb6e-176">Versione di Net Framework</span><span class="sxs-lookup"><span data-stu-id="ddb6e-176">Net Framework Version</span></span>

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

### <span data-ttu-id="ddb6e-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ddb6e-177">-NumberOfWorkers</span></span>
<span data-ttu-id="ddb6e-178">Il numero di lavoratori da allocare</span><span class="sxs-lookup"><span data-stu-id="ddb6e-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ddb6e-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ddb6e-179">-PhpVersion</span></span>
<span data-ttu-id="ddb6e-180">Versione Php</span><span class="sxs-lookup"><span data-stu-id="ddb6e-180">Php Version</span></span>

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

### <span data-ttu-id="ddb6e-181">-RequestTenabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="ddb6e-182">Traccia richiesta abilitata</span><span class="sxs-lookup"><span data-stu-id="ddb6e-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="ddb6e-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb6e-183">-ResourceGroupName</span></span>
<span data-ttu-id="ddb6e-184">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ddb6e-184">Resource Group Name</span></span>

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

### <span data-ttu-id="ddb6e-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ddb6e-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ddb6e-186">Usare la funzione booleana Processo di lavoro a 32 bit</span><span class="sxs-lookup"><span data-stu-id="ddb6e-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="ddb6e-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-187">-WebApp</span></span>
<span data-ttu-id="ddb6e-188">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-188">WebApp Object</span></span>

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

### <span data-ttu-id="ddb6e-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="ddb6e-190">Booleano WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ddb6e-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="ddb6e-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb6e-191">CommonParameters</span></span>
<span data-ttu-id="ddb6e-192">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb6e-193">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb6e-194">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddb6e-194">INPUTS</span></span>

### <span data-ttu-id="ddb6e-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ddb6e-195">System.Int32</span></span>

### <span data-ttu-id="ddb6e-196">System.String</span><span class="sxs-lookup"><span data-stu-id="ddb6e-196">System.String</span></span>

### <span data-ttu-id="ddb6e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ddb6e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ddb6e-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddb6e-198">OUTPUTS</span></span>

### <span data-ttu-id="ddb6e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ddb6e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ddb6e-200">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddb6e-200">NOTES</span></span>
<span data-ttu-id="ddb6e-201">Il cmdlet fornito di seguito aiuta ad aggiornare Azure Web App a **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="ddb6e-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="ddb6e-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="ddb6e-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="ddb6e-203">Sostituire i valori di Default-Web-WestUS con il nome del gruppo di risorse della webapp e di ContosoWebApp con il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="ddb6e-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="ddb6e-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddb6e-204">RELATED LINKS</span></span>

[<span data-ttu-id="ddb6e-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ddb6e-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ddb6e-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ddb6e-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ddb6e-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ddb6e-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ddb6e-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="ddb6e-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="ddb6e-211">New-AzResource</span></span>](./New-AzResource.md)
