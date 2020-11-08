---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192614"
---
# <span data-ttu-id="c5aa8-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c5aa8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aa8-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="c5aa8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5aa8-104">SYNTAX</span></span>

### <span data-ttu-id="c5aa8-105">S1</span><span class="sxs-lookup"><span data-stu-id="c5aa8-105">S1</span></span>
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

### <span data-ttu-id="c5aa8-106">S2</span><span class="sxs-lookup"><span data-stu-id="c5aa8-106">S2</span></span>
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

## <span data-ttu-id="c5aa8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="c5aa8-108">Il cmdlet **set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="c5aa8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="c5aa8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5aa8-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c5aa8-111">Questo comando modifica il piano Appservice associato a Slot001, nella ContosoWebApp web app associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c5aa8-112">Usare il collegamento per altre informazioni su come modificare il piano Appservice e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c5aa8-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c5aa8-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c5aa8-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c5aa8-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="c5aa8-115">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="c5aa8-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c5aa8-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c5aa8-116">Example 3</span></span>

<span data-ttu-id="c5aa8-117">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="c5aa8-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c5aa8-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="c5aa8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5aa8-119">PARAMETERS</span></span>

### <span data-ttu-id="c5aa8-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c5aa8-120">-AlwaysOn</span></span>
<span data-ttu-id="c5aa8-121">Assicurarsi che l'app Web venga caricata per sempre, invece scaricata dopo essere stata inattiva.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c5aa8-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c5aa8-122">-AppServicePlan</span></span>
<span data-ttu-id="c5aa8-123">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="c5aa8-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="c5aa8-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c5aa8-124">-AppSettings</span></span>
<span data-ttu-id="c5aa8-125">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-125">App Settings HashTable.</span></span> <span data-ttu-id="c5aa8-126">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo tutte le impostazioni non fornite.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="c5aa8-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5aa8-127">-AsJob</span></span>
<span data-ttu-id="c5aa8-128">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5aa8-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5aa8-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c5aa8-129">-AssignIdentity</span></span>
<span data-ttu-id="c5aa8-130">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="c5aa8-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="c5aa8-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c5aa8-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="c5aa8-132">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="c5aa8-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c5aa8-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c5aa8-133">-AzureStoragePath</span></span>
<span data-ttu-id="c5aa8-134">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c5aa8-135">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="c5aa8-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c5aa8-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c5aa8-136">-ConnectionStrings</span></span>
<span data-ttu-id="c5aa8-137">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="c5aa8-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c5aa8-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c5aa8-138">-ContainerImageName</span></span>
<span data-ttu-id="c5aa8-139">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="c5aa8-139">Container Image Name</span></span>

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

### <span data-ttu-id="c5aa8-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c5aa8-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c5aa8-141">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="c5aa8-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c5aa8-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c5aa8-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c5aa8-143">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="c5aa8-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c5aa8-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c5aa8-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="c5aa8-145">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="c5aa8-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c5aa8-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c5aa8-146">-DefaultDocuments</span></span>
<span data-ttu-id="c5aa8-147">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="c5aa8-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="c5aa8-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aa8-148">-DefaultProfile</span></span>
<span data-ttu-id="c5aa8-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5aa8-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c5aa8-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c5aa8-151">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="c5aa8-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c5aa8-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c5aa8-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c5aa8-153">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="c5aa8-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c5aa8-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c5aa8-154">-FtpsState</span></span>
<span data-ttu-id="c5aa8-155">Imposta il valore di stato FTPS per un'app.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c5aa8-156">Valori consentiti [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c5aa8-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c5aa8-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c5aa8-157">-HandlerMappings</span></span>
<span data-ttu-id="c5aa8-158">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="c5aa8-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c5aa8-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c5aa8-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c5aa8-160">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="c5aa8-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c5aa8-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c5aa8-161">-HttpsOnly</span></span>
<span data-ttu-id="c5aa8-162">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="c5aa8-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="c5aa8-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c5aa8-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="c5aa8-164">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="c5aa8-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c5aa8-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c5aa8-165">-MinTlsVersion</span></span>
<span data-ttu-id="c5aa8-166">La versione minima di TLS necessaria per le richieste SSL.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c5aa8-167">Valori consentiti [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c5aa8-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c5aa8-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5aa8-168">-Name</span></span>
<span data-ttu-id="c5aa8-169">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="c5aa8-169">WebApp Name</span></span>

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

### <span data-ttu-id="c5aa8-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c5aa8-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="c5aa8-171">NET Framework</span><span class="sxs-lookup"><span data-stu-id="c5aa8-171">Net Framework Version</span></span>

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

### <span data-ttu-id="c5aa8-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c5aa8-172">-NumberOfWorkers</span></span>
<span data-ttu-id="c5aa8-173">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="c5aa8-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c5aa8-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c5aa8-174">-PhpVersion</span></span>
<span data-ttu-id="c5aa8-175">Versione php</span><span class="sxs-lookup"><span data-stu-id="c5aa8-175">Php Version</span></span>

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

### <span data-ttu-id="c5aa8-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c5aa8-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="c5aa8-177">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="c5aa8-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="c5aa8-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aa8-178">-ResourceGroupName</span></span>
<span data-ttu-id="c5aa8-179">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c5aa8-179">Resource Group Name</span></span>

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

### <span data-ttu-id="c5aa8-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-180">-Slot</span></span>
<span data-ttu-id="c5aa8-181">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="c5aa8-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c5aa8-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c5aa8-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c5aa8-183">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="c5aa8-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c5aa8-184">-Web App</span><span class="sxs-lookup"><span data-stu-id="c5aa8-184">-WebApp</span></span>
<span data-ttu-id="c5aa8-185">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="c5aa8-185">WebApp Object</span></span>

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

### <span data-ttu-id="c5aa8-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c5aa8-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="c5aa8-187">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="c5aa8-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="c5aa8-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aa8-188">CommonParameters</span></span>
<span data-ttu-id="c5aa8-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aa8-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5aa8-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aa8-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5aa8-191">INPUTS</span></span>

### <span data-ttu-id="c5aa8-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c5aa8-192">System.Int32</span></span>

### <span data-ttu-id="c5aa8-193">System. String</span><span class="sxs-lookup"><span data-stu-id="c5aa8-193">System.String</span></span>

### <span data-ttu-id="c5aa8-194">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c5aa8-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5aa8-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5aa8-195">OUTPUTS</span></span>

### <span data-ttu-id="c5aa8-196">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c5aa8-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5aa8-197">Note</span><span class="sxs-lookup"><span data-stu-id="c5aa8-197">NOTES</span></span>

## <span data-ttu-id="c5aa8-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5aa8-198">RELATED LINKS</span></span>

[<span data-ttu-id="c5aa8-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-202">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c5aa8-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c5aa8-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c5aa8-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)