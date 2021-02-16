---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 46c5dae54bf4f59556e62256797a43221d0650b7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412351"
---
# <span data-ttu-id="6a937-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-101">Set-AzWebApp</span></span>

## <span data-ttu-id="6a937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a937-102">SYNOPSIS</span></span>
<span data-ttu-id="6a937-103">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a937-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="6a937-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a937-104">SYNTAX</span></span>

### <span data-ttu-id="6a937-105">S1</span><span class="sxs-lookup"><span data-stu-id="6a937-105">S1</span></span>
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

### <span data-ttu-id="6a937-106">S2</span><span class="sxs-lookup"><span data-stu-id="6a937-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a937-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a937-107">DESCRIPTION</span></span>
<span data-ttu-id="6a937-108">Il cmdlet **Set-AzWebApp** imposta un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a937-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="6a937-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a937-109">EXAMPLES</span></span>

### <span data-ttu-id="6a937-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a937-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="6a937-111">Questo comando modifica il piano di servizio app associato all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6a937-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="6a937-112">Usare il collegamento per altre informazioni su come modificare il piano di servizio app e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="6a937-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="6a937-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="6a937-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="6a937-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a937-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="6a937-115">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="6a937-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="6a937-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6a937-116">Example 3</span></span>

<span data-ttu-id="6a937-117">Modifica un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a937-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="6a937-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="6a937-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="6a937-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a937-119">PARAMETERS</span></span>

### <span data-ttu-id="6a937-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="6a937-120">-AlwaysOn</span></span>
<span data-ttu-id="6a937-121">Assicurarsi che l'app Web venga caricata di tanto in tanto, piuttosto che dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="6a937-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="6a937-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6a937-122">-AppServicePlan</span></span>
<span data-ttu-id="6a937-123">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="6a937-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="6a937-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="6a937-124">-AppSettings</span></span>
<span data-ttu-id="6a937-125">Tabella HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="6a937-125">App Settings HashTable.</span></span> <span data-ttu-id="6a937-126">Le impostazioni delle app esistenti verranno sostituite, rimuovendo quelle non disponibili.</span><span class="sxs-lookup"><span data-stu-id="6a937-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="6a937-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a937-127">-AsJob</span></span>
<span data-ttu-id="6a937-128">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6a937-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a937-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6a937-129">-AssignIdentity</span></span>
<span data-ttu-id="6a937-130">Abilitare/disabilitare MSI in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="6a937-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="6a937-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="6a937-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="6a937-132">Nome slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="6a937-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="6a937-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="6a937-133">-AzureStoragePath</span></span>
<span data-ttu-id="6a937-134">Archiviazione di Azure per il montaggio all'interno di un'app Web per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a937-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="6a937-135">Usare New-AzureRmWebAppAzureStoragePath per crearla</span><span class="sxs-lookup"><span data-stu-id="6a937-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="6a937-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="6a937-136">-ConnectionStrings</span></span>
<span data-ttu-id="6a937-137">Tabella HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="6a937-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="6a937-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="6a937-138">-ContainerImageName</span></span>
<span data-ttu-id="6a937-139">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="6a937-139">Container Image Name</span></span>

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

### <span data-ttu-id="6a937-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="6a937-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="6a937-141">Password del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="6a937-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="6a937-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="6a937-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="6a937-143">Url del server del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="6a937-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="6a937-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="6a937-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="6a937-145">Nome utente del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="6a937-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="6a937-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="6a937-146">-DefaultDocuments</span></span>
<span data-ttu-id="6a937-147">Matrice stringa documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="6a937-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="6a937-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a937-148">-DefaultProfile</span></span>
<span data-ttu-id="6a937-149">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a937-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a937-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a937-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="6a937-151">Booleano di registrazione degli errori dettagliato abilitato</span><span class="sxs-lookup"><span data-stu-id="6a937-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="6a937-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="6a937-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="6a937-153">Abilita/disabilita il webhook della distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="6a937-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="6a937-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="6a937-154">-FtpsState</span></span>
<span data-ttu-id="6a937-155">Impostare il valore dello stato ftp per un'app.</span><span class="sxs-lookup"><span data-stu-id="6a937-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="6a937-156">Valori consentiti [AllAllowed | Disabilitato | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="6a937-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="6a937-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="6a937-157">-HandlerMappings</span></span>
<span data-ttu-id="6a937-158">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="6a937-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="6a937-159">-HostNames</span><span class="sxs-lookup"><span data-stu-id="6a937-159">-HostNames</span></span>
<span data-ttu-id="6a937-160">Matrice stringa HostNames della WebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="6a937-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a937-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="6a937-162">Booleano HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a937-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="6a937-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6a937-163">-HttpsOnly</span></span>
<span data-ttu-id="6a937-164">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un'app Web o una functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="6a937-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="6a937-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="6a937-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="6a937-166">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="6a937-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="6a937-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6a937-167">-MinTlsVersion</span></span>
<span data-ttu-id="6a937-168">Versione minima di TLS richiesta per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="6a937-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="6a937-169">Valori consentiti [1,0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="6a937-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="6a937-170">-Name</span><span class="sxs-lookup"><span data-stu-id="6a937-170">-Name</span></span>
<span data-ttu-id="6a937-171">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-171">WebApp Name</span></span>

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

### <span data-ttu-id="6a937-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="6a937-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="6a937-173">Versione di Net Framework</span><span class="sxs-lookup"><span data-stu-id="6a937-173">Net Framework Version</span></span>

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

### <span data-ttu-id="6a937-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="6a937-174">-NumberOfWorkers</span></span>
<span data-ttu-id="6a937-175">Il numero di lavoratori da allocare</span><span class="sxs-lookup"><span data-stu-id="6a937-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="6a937-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="6a937-176">-PhpVersion</span></span>
<span data-ttu-id="6a937-177">Versione Php</span><span class="sxs-lookup"><span data-stu-id="6a937-177">Php Version</span></span>

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

### <span data-ttu-id="6a937-178">-RequestTenabled</span><span class="sxs-lookup"><span data-stu-id="6a937-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="6a937-179">Traccia richiesta abilitata</span><span class="sxs-lookup"><span data-stu-id="6a937-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="6a937-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a937-180">-ResourceGroupName</span></span>
<span data-ttu-id="6a937-181">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6a937-181">Resource Group Name</span></span>

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

### <span data-ttu-id="6a937-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="6a937-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="6a937-183">Usare la funzione booleana Processo di lavoro a 32 bit</span><span class="sxs-lookup"><span data-stu-id="6a937-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="6a937-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-184">-WebApp</span></span>
<span data-ttu-id="6a937-185">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-185">WebApp Object</span></span>

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

### <span data-ttu-id="6a937-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a937-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="6a937-187">Booleano WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a937-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="6a937-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a937-188">CommonParameters</span></span>
<span data-ttu-id="6a937-189">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a937-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a937-190">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a937-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a937-191">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a937-191">INPUTS</span></span>

### <span data-ttu-id="6a937-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6a937-192">System.Int32</span></span>

### <span data-ttu-id="6a937-193">System.String</span><span class="sxs-lookup"><span data-stu-id="6a937-193">System.String</span></span>

### <span data-ttu-id="6a937-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6a937-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6a937-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a937-195">OUTPUTS</span></span>

### <span data-ttu-id="6a937-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6a937-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6a937-197">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a937-197">NOTES</span></span>
<span data-ttu-id="6a937-198">Il cmdlet fornito di seguito aiuta ad aggiornare Azure Web App a **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="6a937-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="6a937-199">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="6a937-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="6a937-200">Sostituire i valori di Default-Web-WestUS con il nome del gruppo di risorse dell'app Web e di ContosoWebApp con il nome della webapp.</span><span class="sxs-lookup"><span data-stu-id="6a937-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="6a937-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a937-201">RELATED LINKS</span></span>

[<span data-ttu-id="6a937-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="6a937-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="6a937-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="6a937-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="6a937-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="6a937-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a937-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

