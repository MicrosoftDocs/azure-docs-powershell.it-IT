---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011102"
---
# <span data-ttu-id="b04c7-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="b04c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b04c7-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b04c7-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="b04c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b04c7-104">SYNTAX</span></span>

### <span data-ttu-id="b04c7-105">S1</span><span class="sxs-lookup"><span data-stu-id="b04c7-105">S1</span></span>
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

### <span data-ttu-id="b04c7-106">S2</span><span class="sxs-lookup"><span data-stu-id="b04c7-106">S2</span></span>
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

## <span data-ttu-id="b04c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b04c7-107">DESCRIPTION</span></span>
<span data-ttu-id="b04c7-108">Il cmdlet **Set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b04c7-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="b04c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b04c7-109">EXAMPLES</span></span>

### <span data-ttu-id="b04c7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b04c7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="b04c7-111">Questo comando modifica il piano di servizio app associato a Slot001 nell'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b04c7-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="b04c7-112">Usare il collegamento per altre informazioni su come modificare il piano di servizio app e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="b04c7-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="b04c7-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="b04c7-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="b04c7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b04c7-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="b04c7-115">Questo comando imposta HttpLoggingEnabled su true per slot slot001 relativo all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="b04c7-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="b04c7-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b04c7-116">Example 3</span></span>

<span data-ttu-id="b04c7-117">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b04c7-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="b04c7-118">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="b04c7-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="b04c7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b04c7-119">PARAMETERS</span></span>

### <span data-ttu-id="b04c7-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="b04c7-120">-AlwaysOn</span></span>
<span data-ttu-id="b04c7-121">Assicurarsi che l'app Web venga caricata di tanto in tanto, piuttosto che dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="b04c7-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="b04c7-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b04c7-122">-AppServicePlan</span></span>
<span data-ttu-id="b04c7-123">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="b04c7-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="b04c7-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="b04c7-124">-AppSettings</span></span>
<span data-ttu-id="b04c7-125">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="b04c7-125">App Settings HashTable.</span></span> <span data-ttu-id="b04c7-126">Le impostazioni delle app esistenti verranno sostituite, rimuovendo quelle non disponibili.</span><span class="sxs-lookup"><span data-stu-id="b04c7-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="b04c7-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b04c7-127">-AsJob</span></span>
<span data-ttu-id="b04c7-128">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b04c7-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b04c7-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b04c7-129">-AssignIdentity</span></span>
<span data-ttu-id="b04c7-130">Abilitare/disabilitare MSI in uno slot esistente [ANTEPRIMA]</span><span class="sxs-lookup"><span data-stu-id="b04c7-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="b04c7-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="b04c7-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="b04c7-132">Nome slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="b04c7-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="b04c7-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="b04c7-133">-AzureStoragePath</span></span>
<span data-ttu-id="b04c7-134">Archiviazione di Azure per il montaggio all'interno di un'app Web per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="b04c7-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="b04c7-135">Usare New-AzureRmWebAppAzureStoragePath per crearla</span><span class="sxs-lookup"><span data-stu-id="b04c7-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="b04c7-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b04c7-136">-ConnectionStrings</span></span>
<span data-ttu-id="b04c7-137">Tabella HashTable delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="b04c7-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="b04c7-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="b04c7-138">-ContainerImageName</span></span>
<span data-ttu-id="b04c7-139">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="b04c7-139">Container Image Name</span></span>

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

### <span data-ttu-id="b04c7-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="b04c7-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="b04c7-141">Password del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="b04c7-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="b04c7-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="b04c7-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="b04c7-143">URL del server del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="b04c7-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="b04c7-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="b04c7-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="b04c7-145">Nome utente del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="b04c7-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="b04c7-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="b04c7-146">-DefaultDocuments</span></span>
<span data-ttu-id="b04c7-147">Matrice di stringhe di documenti predefinite</span><span class="sxs-lookup"><span data-stu-id="b04c7-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="b04c7-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04c7-148">-DefaultProfile</span></span>
<span data-ttu-id="b04c7-149">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b04c7-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04c7-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="b04c7-151">Booleano registrazione errori dettagliato abilitato</span><span class="sxs-lookup"><span data-stu-id="b04c7-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="b04c7-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="b04c7-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="b04c7-153">Abilita/disabilita il webhook della distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="b04c7-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="b04c7-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="b04c7-154">-FtpsState</span></span>
<span data-ttu-id="b04c7-155">Impostare il valore dello stato ftp per un'app.</span><span class="sxs-lookup"><span data-stu-id="b04c7-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="b04c7-156">Valori consentiti [AllAllowed | Disabilitato | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="b04c7-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="b04c7-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="b04c7-157">-HandlerMappings</span></span>
<span data-ttu-id="b04c7-158">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="b04c7-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="b04c7-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="b04c7-160">Booleano HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="b04c7-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b04c7-161">-HttpsOnly</span></span>
<span data-ttu-id="b04c7-162">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="b04c7-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="b04c7-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="b04c7-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="b04c7-164">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="b04c7-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="b04c7-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b04c7-165">-MinTlsVersion</span></span>
<span data-ttu-id="b04c7-166">La versione minima di TLS richiesta per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="b04c7-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="b04c7-167">Valori consentiti [1,0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="b04c7-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="b04c7-168">-Name</span><span class="sxs-lookup"><span data-stu-id="b04c7-168">-Name</span></span>
<span data-ttu-id="b04c7-169">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="b04c7-169">WebApp Name</span></span>

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

### <span data-ttu-id="b04c7-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="b04c7-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="b04c7-171">Versione di Net Framework</span><span class="sxs-lookup"><span data-stu-id="b04c7-171">Net Framework Version</span></span>

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

### <span data-ttu-id="b04c7-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="b04c7-172">-NumberOfWorkers</span></span>
<span data-ttu-id="b04c7-173">Il numero di lavoratori da allocare</span><span class="sxs-lookup"><span data-stu-id="b04c7-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="b04c7-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="b04c7-174">-PhpVersion</span></span>
<span data-ttu-id="b04c7-175">Versione Php</span><span class="sxs-lookup"><span data-stu-id="b04c7-175">Php Version</span></span>

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

### <span data-ttu-id="b04c7-176">-RequestTenabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="b04c7-177">Booleano Request Tracing Enabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="b04c7-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04c7-178">-ResourceGroupName</span></span>
<span data-ttu-id="b04c7-179">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b04c7-179">Resource Group Name</span></span>

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

### <span data-ttu-id="b04c7-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="b04c7-180">-Slot</span></span>
<span data-ttu-id="b04c7-181">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="b04c7-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b04c7-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="b04c7-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="b04c7-183">Usare la funzione booleana Processo di lavoro a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b04c7-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="b04c7-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b04c7-184">-WebApp</span></span>
<span data-ttu-id="b04c7-185">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="b04c7-185">WebApp Object</span></span>

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

### <span data-ttu-id="b04c7-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b04c7-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="b04c7-187">Booleano abilitato per Web Sockets</span><span class="sxs-lookup"><span data-stu-id="b04c7-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="b04c7-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04c7-188">CommonParameters</span></span>
<span data-ttu-id="b04c7-189">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04c7-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04c7-190">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b04c7-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04c7-191">INPUT</span><span class="sxs-lookup"><span data-stu-id="b04c7-191">INPUTS</span></span>

### <span data-ttu-id="b04c7-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b04c7-192">System.Int32</span></span>

### <span data-ttu-id="b04c7-193">System.String</span><span class="sxs-lookup"><span data-stu-id="b04c7-193">System.String</span></span>

### <span data-ttu-id="b04c7-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b04c7-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b04c7-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b04c7-195">OUTPUTS</span></span>

### <span data-ttu-id="b04c7-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b04c7-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b04c7-197">NOTE</span><span class="sxs-lookup"><span data-stu-id="b04c7-197">NOTES</span></span>

## <span data-ttu-id="b04c7-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b04c7-198">RELATED LINKS</span></span>

[<span data-ttu-id="b04c7-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b04c7-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b04c7-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b04c7-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
