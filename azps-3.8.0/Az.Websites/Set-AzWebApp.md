---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020860"
---
# <span data-ttu-id="6a667-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-101">Set-AzWebApp</span></span>

## <span data-ttu-id="6a667-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a667-102">SYNOPSIS</span></span>
<span data-ttu-id="6a667-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="6a667-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="6a667-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a667-104">SYNTAX</span></span>

### <span data-ttu-id="6a667-105">S1</span><span class="sxs-lookup"><span data-stu-id="6a667-105">S1</span></span>
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

### <span data-ttu-id="6a667-106">S2</span><span class="sxs-lookup"><span data-stu-id="6a667-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a667-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a667-107">DESCRIPTION</span></span>
<span data-ttu-id="6a667-108">Il cmdlet **set-AzWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6a667-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="6a667-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a667-109">EXAMPLES</span></span>

### <span data-ttu-id="6a667-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a667-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="6a667-111">Questo comando modifica il piano Appservice associato all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6a667-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="6a667-112">Usare il collegamento per altre informazioni su come modificare il piano Appservice e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="6a667-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="6a667-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="6a667-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="6a667-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a667-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="6a667-115">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="6a667-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6a667-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a667-116">PARAMETERS</span></span>

### <span data-ttu-id="6a667-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="6a667-117">-AlwaysOn</span></span>
<span data-ttu-id="6a667-118">Assicurarsi che l'app Web venga caricata per sempre, invece scaricata dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="6a667-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="6a667-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6a667-119">-AppServicePlan</span></span>
<span data-ttu-id="6a667-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="6a667-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="6a667-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="6a667-121">-AppSettings</span></span>
<span data-ttu-id="6a667-122">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="6a667-122">App Settings HashTable.</span></span> <span data-ttu-id="6a667-123">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo tutte le impostazioni non fornite.</span><span class="sxs-lookup"><span data-stu-id="6a667-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="6a667-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a667-124">-AsJob</span></span>
<span data-ttu-id="6a667-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6a667-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a667-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6a667-126">-AssignIdentity</span></span>
<span data-ttu-id="6a667-127">Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="6a667-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="6a667-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="6a667-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="6a667-129">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="6a667-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="6a667-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="6a667-130">-AzureStoragePath</span></span>
<span data-ttu-id="6a667-131">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="6a667-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="6a667-132">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="6a667-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="6a667-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="6a667-133">-ConnectionStrings</span></span>
<span data-ttu-id="6a667-134">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="6a667-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="6a667-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="6a667-135">-ContainerImageName</span></span>
<span data-ttu-id="6a667-136">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="6a667-136">Container Image Name</span></span>

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

### <span data-ttu-id="6a667-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="6a667-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="6a667-138">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="6a667-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="6a667-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="6a667-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="6a667-140">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="6a667-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="6a667-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="6a667-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="6a667-142">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="6a667-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="6a667-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="6a667-143">-DefaultDocuments</span></span>
<span data-ttu-id="6a667-144">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="6a667-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="6a667-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a667-145">-DefaultProfile</span></span>
<span data-ttu-id="6a667-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a667-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a667-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a667-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="6a667-148">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="6a667-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="6a667-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="6a667-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="6a667-150">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="6a667-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="6a667-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="6a667-151">-FtpsState</span></span>
<span data-ttu-id="6a667-152">Imposta il valore di stato FTPS per un'app.</span><span class="sxs-lookup"><span data-stu-id="6a667-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="6a667-153">Valori consentiti [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="6a667-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="6a667-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="6a667-154">-HandlerMappings</span></span>
<span data-ttu-id="6a667-155">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="6a667-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="6a667-156">-HostName</span><span class="sxs-lookup"><span data-stu-id="6a667-156">-HostNames</span></span>
<span data-ttu-id="6a667-157">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="6a667-157">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="6a667-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a667-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="6a667-159">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="6a667-159">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="6a667-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6a667-160">-HttpsOnly</span></span>
<span data-ttu-id="6a667-161">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente</span><span class="sxs-lookup"><span data-stu-id="6a667-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="6a667-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="6a667-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="6a667-163">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="6a667-163">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="6a667-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6a667-164">-MinTlsVersion</span></span>
<span data-ttu-id="6a667-165">La versione minima di TLS necessaria per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="6a667-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="6a667-166">Valori consentiti [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="6a667-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="6a667-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a667-167">-Name</span></span>
<span data-ttu-id="6a667-168">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="6a667-168">WebApp Name</span></span>

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

### <span data-ttu-id="6a667-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="6a667-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="6a667-170">NET Framework</span><span class="sxs-lookup"><span data-stu-id="6a667-170">Net Framework Version</span></span>

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

### <span data-ttu-id="6a667-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="6a667-171">-NumberOfWorkers</span></span>
<span data-ttu-id="6a667-172">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="6a667-172">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="6a667-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="6a667-173">-PhpVersion</span></span>
<span data-ttu-id="6a667-174">Versione php</span><span class="sxs-lookup"><span data-stu-id="6a667-174">Php Version</span></span>

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

### <span data-ttu-id="6a667-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="6a667-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="6a667-176">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="6a667-176">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="6a667-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a667-177">-ResourceGroupName</span></span>
<span data-ttu-id="6a667-178">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6a667-178">Resource Group Name</span></span>

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

### <span data-ttu-id="6a667-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="6a667-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="6a667-180">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="6a667-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="6a667-181">-Web App</span><span class="sxs-lookup"><span data-stu-id="6a667-181">-WebApp</span></span>
<span data-ttu-id="6a667-182">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="6a667-182">WebApp Object</span></span>

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

### <span data-ttu-id="6a667-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a667-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="6a667-184">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="6a667-184">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="6a667-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a667-185">CommonParameters</span></span>
<span data-ttu-id="6a667-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a667-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a667-187">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a667-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a667-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a667-188">INPUTS</span></span>

### <span data-ttu-id="6a667-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6a667-189">System.Int32</span></span>

### <span data-ttu-id="6a667-190">System. String</span><span class="sxs-lookup"><span data-stu-id="6a667-190">System.String</span></span>

### <span data-ttu-id="6a667-191">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6a667-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6a667-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a667-192">OUTPUTS</span></span>

### <span data-ttu-id="6a667-193">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6a667-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6a667-194">Note</span><span class="sxs-lookup"><span data-stu-id="6a667-194">NOTES</span></span>

## <span data-ttu-id="6a667-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a667-195">RELATED LINKS</span></span>

[<span data-ttu-id="6a667-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="6a667-197">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="6a667-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="6a667-199">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="6a667-200">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="6a667-201">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a667-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
