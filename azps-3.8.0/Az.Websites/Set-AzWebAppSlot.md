---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020559"
---
# <span data-ttu-id="ed0a2-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="ed0a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0a2-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="ed0a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed0a2-104">SYNTAX</span></span>

### <span data-ttu-id="ed0a2-105">S1</span><span class="sxs-lookup"><span data-stu-id="ed0a2-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed0a2-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed0a2-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed0a2-107">DESCRIPTION</span></span>
<span data-ttu-id="ed0a2-108">Il cmdlet **set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="ed0a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed0a2-109">EXAMPLES</span></span>

### <span data-ttu-id="ed0a2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed0a2-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="ed0a2-111">Questo comando modifica il piano Appservice associato a Slot001, nella ContosoWebApp web app associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ed0a2-112">Usare il collegamento per altre informazioni su come modificare il piano Appservice e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="ed0a2-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="ed0a2-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="ed0a2-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ed0a2-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="ed0a2-115">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ed0a2-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ed0a2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed0a2-116">PARAMETERS</span></span>

### <span data-ttu-id="ed0a2-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="ed0a2-117">-AlwaysOn</span></span>
<span data-ttu-id="ed0a2-118">Assicurarsi che l'app Web venga caricata per sempre, invece scaricata dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="ed0a2-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed0a2-119">-AppServicePlan</span></span>
<span data-ttu-id="ed0a2-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ed0a2-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ed0a2-121">-AppSettings</span></span>
<span data-ttu-id="ed0a2-122">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-122">App Settings HashTable.</span></span> <span data-ttu-id="ed0a2-123">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo tutte le impostazioni non fornite.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed0a2-124">-AsJob</span></span>
<span data-ttu-id="ed0a2-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed0a2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed0a2-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ed0a2-126">-AssignIdentity</span></span>
<span data-ttu-id="ed0a2-127">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="ed0a2-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="ed0a2-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ed0a2-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="ed0a2-129">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="ed0a2-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ed0a2-130">-AzureStoragePath</span></span>
<span data-ttu-id="ed0a2-131">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="ed0a2-132">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="ed0a2-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="ed0a2-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ed0a2-133">-ConnectionStrings</span></span>
<span data-ttu-id="ed0a2-134">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="ed0a2-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ed0a2-135">-ContainerImageName</span></span>
<span data-ttu-id="ed0a2-136">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="ed0a2-136">Container Image Name</span></span>

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

### <span data-ttu-id="ed0a2-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ed0a2-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ed0a2-138">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ed0a2-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="ed0a2-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ed0a2-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ed0a2-140">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ed0a2-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="ed0a2-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ed0a2-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="ed0a2-142">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ed0a2-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="ed0a2-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ed0a2-143">-DefaultDocuments</span></span>
<span data-ttu-id="ed0a2-144">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="ed0a2-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0a2-145">-DefaultProfile</span></span>
<span data-ttu-id="ed0a2-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0a2-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed0a2-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ed0a2-148">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="ed0a2-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ed0a2-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ed0a2-150">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="ed0a2-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ed0a2-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="ed0a2-151">-FtpsState</span></span>
<span data-ttu-id="ed0a2-152">Imposta il valore di stato FTPS per un'app.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="ed0a2-153">Valori consentiti [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="ed0a2-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="ed0a2-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ed0a2-154">-HandlerMappings</span></span>
<span data-ttu-id="ed0a2-155">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="ed0a2-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed0a2-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ed0a2-157">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ed0a2-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ed0a2-158">-HttpsOnly</span></span>
<span data-ttu-id="ed0a2-159">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="ed0a2-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="ed0a2-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ed0a2-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="ed0a2-161">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="ed0a2-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ed0a2-162">-MinTlsVersion</span></span>
<span data-ttu-id="ed0a2-163">La versione minima di TLS necessaria per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="ed0a2-164">Valori consentiti [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="ed0a2-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="ed0a2-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed0a2-165">-Name</span></span>
<span data-ttu-id="ed0a2-166">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ed0a2-166">WebApp Name</span></span>

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

### <span data-ttu-id="ed0a2-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ed0a2-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="ed0a2-168">NET Framework</span><span class="sxs-lookup"><span data-stu-id="ed0a2-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ed0a2-169">-NumberOfWorkers</span></span>
<span data-ttu-id="ed0a2-170">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="ed0a2-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ed0a2-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ed0a2-171">-PhpVersion</span></span>
<span data-ttu-id="ed0a2-172">Versione php</span><span class="sxs-lookup"><span data-stu-id="ed0a2-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ed0a2-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="ed0a2-174">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="ed0a2-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0a2-175">-ResourceGroupName</span></span>
<span data-ttu-id="ed0a2-176">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ed0a2-176">Resource Group Name</span></span>

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

### <span data-ttu-id="ed0a2-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-177">-Slot</span></span>
<span data-ttu-id="ed0a2-178">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ed0a2-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ed0a2-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ed0a2-180">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="ed0a2-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a2-181">-Web App</span><span class="sxs-lookup"><span data-stu-id="ed0a2-181">-WebApp</span></span>
<span data-ttu-id="ed0a2-182">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ed0a2-182">WebApp Object</span></span>

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

### <span data-ttu-id="ed0a2-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ed0a2-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="ed0a2-184">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="ed0a2-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="ed0a2-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0a2-185">CommonParameters</span></span>
<span data-ttu-id="ed0a2-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0a2-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0a2-187">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed0a2-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0a2-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed0a2-188">INPUTS</span></span>

### <span data-ttu-id="ed0a2-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ed0a2-189">System.Int32</span></span>

### <span data-ttu-id="ed0a2-190">System. String</span><span class="sxs-lookup"><span data-stu-id="ed0a2-190">System.String</span></span>

### <span data-ttu-id="ed0a2-191">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ed0a2-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed0a2-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed0a2-192">OUTPUTS</span></span>

### <span data-ttu-id="ed0a2-193">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ed0a2-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed0a2-194">Note</span><span class="sxs-lookup"><span data-stu-id="ed0a2-194">NOTES</span></span>

## <span data-ttu-id="ed0a2-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed0a2-195">RELATED LINKS</span></span>

[<span data-ttu-id="ed0a2-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-197">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-199">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-200">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-201">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed0a2-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ed0a2-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ed0a2-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
