---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858654"
---
# <span data-ttu-id="54fe9-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="54fe9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="54fe9-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="54fe9-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="54fe9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54fe9-104">SYNTAX</span></span>

### <span data-ttu-id="54fe9-105">S1</span><span class="sxs-lookup"><span data-stu-id="54fe9-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fe9-106">S2</span><span class="sxs-lookup"><span data-stu-id="54fe9-106">S2</span></span>
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

## <span data-ttu-id="54fe9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54fe9-107">DESCRIPTION</span></span>
<span data-ttu-id="54fe9-108">Il cmdlet **set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="54fe9-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="54fe9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54fe9-109">EXAMPLES</span></span>

### <span data-ttu-id="54fe9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54fe9-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="54fe9-111">Questo comando modifica il piano Appservice associato a Slot001, nella ContosoWebApp web app associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="54fe9-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="54fe9-112">Usare il collegamento per altre informazioni su come modificare il piano Appservice e i vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="54fe9-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="54fe9-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="54fe9-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="54fe9-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="54fe9-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="54fe9-115">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="54fe9-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="54fe9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54fe9-116">PARAMETERS</span></span>

### <span data-ttu-id="54fe9-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="54fe9-117">-AppServicePlan</span></span>
<span data-ttu-id="54fe9-118">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="54fe9-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="54fe9-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="54fe9-119">-AppSettings</span></span>
<span data-ttu-id="54fe9-120">HashTable delle impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="54fe9-120">App Settings HashTable.</span></span> <span data-ttu-id="54fe9-121">Le impostazioni dell'app esistenti verranno sostituite, rimuovendo tutte le impostazioni non fornite.</span><span class="sxs-lookup"><span data-stu-id="54fe9-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="54fe9-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fe9-122">-AsJob</span></span>
<span data-ttu-id="54fe9-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="54fe9-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54fe9-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="54fe9-124">-AssignIdentity</span></span>
<span data-ttu-id="54fe9-125">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="54fe9-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="54fe9-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="54fe9-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="54fe9-127">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="54fe9-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="54fe9-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="54fe9-128">-AzureStoragePath</span></span>
<span data-ttu-id="54fe9-129">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="54fe9-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="54fe9-130">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="54fe9-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="54fe9-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="54fe9-131">-ConnectionStrings</span></span>
<span data-ttu-id="54fe9-132">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="54fe9-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="54fe9-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="54fe9-133">-ContainerImageName</span></span>
<span data-ttu-id="54fe9-134">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="54fe9-134">Container Image Name</span></span>

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

### <span data-ttu-id="54fe9-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="54fe9-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="54fe9-136">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="54fe9-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="54fe9-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="54fe9-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="54fe9-138">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="54fe9-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="54fe9-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="54fe9-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="54fe9-140">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="54fe9-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="54fe9-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="54fe9-141">-DefaultDocuments</span></span>
<span data-ttu-id="54fe9-142">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="54fe9-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="54fe9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fe9-143">-DefaultProfile</span></span>
<span data-ttu-id="54fe9-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54fe9-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fe9-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="54fe9-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="54fe9-146">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="54fe9-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="54fe9-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="54fe9-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="54fe9-148">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="54fe9-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="54fe9-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="54fe9-149">-HandlerMappings</span></span>
<span data-ttu-id="54fe9-150">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="54fe9-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="54fe9-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="54fe9-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="54fe9-152">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="54fe9-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="54fe9-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="54fe9-153">-HttpsOnly</span></span>
<span data-ttu-id="54fe9-154">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="54fe9-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="54fe9-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="54fe9-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="54fe9-156">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="54fe9-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="54fe9-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="54fe9-157">-Name</span></span>
<span data-ttu-id="54fe9-158">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="54fe9-158">WebApp Name</span></span>

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

### <span data-ttu-id="54fe9-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="54fe9-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="54fe9-160">NET Framework</span><span class="sxs-lookup"><span data-stu-id="54fe9-160">Net Framework Version</span></span>

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

### <span data-ttu-id="54fe9-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="54fe9-161">-NumberOfWorkers</span></span>
<span data-ttu-id="54fe9-162">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="54fe9-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="54fe9-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="54fe9-163">-PhpVersion</span></span>
<span data-ttu-id="54fe9-164">Versione php</span><span class="sxs-lookup"><span data-stu-id="54fe9-164">Php Version</span></span>

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

### <span data-ttu-id="54fe9-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="54fe9-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="54fe9-166">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="54fe9-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="54fe9-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fe9-167">-ResourceGroupName</span></span>
<span data-ttu-id="54fe9-168">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="54fe9-168">Resource Group Name</span></span>

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

### <span data-ttu-id="54fe9-169">-Slot</span><span class="sxs-lookup"><span data-stu-id="54fe9-169">-Slot</span></span>
<span data-ttu-id="54fe9-170">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="54fe9-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="54fe9-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="54fe9-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="54fe9-172">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="54fe9-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="54fe9-173">-Web App</span><span class="sxs-lookup"><span data-stu-id="54fe9-173">-WebApp</span></span>
<span data-ttu-id="54fe9-174">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="54fe9-174">WebApp Object</span></span>

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

### <span data-ttu-id="54fe9-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="54fe9-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="54fe9-176">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="54fe9-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="54fe9-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fe9-177">CommonParameters</span></span>
<span data-ttu-id="54fe9-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54fe9-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fe9-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fe9-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fe9-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54fe9-180">INPUTS</span></span>

### <span data-ttu-id="54fe9-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="54fe9-181">System.Int32</span></span>

### <span data-ttu-id="54fe9-182">System. String</span><span class="sxs-lookup"><span data-stu-id="54fe9-182">System.String</span></span>

### <span data-ttu-id="54fe9-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="54fe9-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="54fe9-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54fe9-184">OUTPUTS</span></span>

### <span data-ttu-id="54fe9-185">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="54fe9-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="54fe9-186">Note</span><span class="sxs-lookup"><span data-stu-id="54fe9-186">NOTES</span></span>

## <span data-ttu-id="54fe9-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54fe9-187">RELATED LINKS</span></span>

[<span data-ttu-id="54fe9-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-189">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-191">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-192">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-193">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54fe9-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="54fe9-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="54fe9-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
