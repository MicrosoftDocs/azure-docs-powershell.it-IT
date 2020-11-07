---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676251"
---
# <span data-ttu-id="3e853-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="3e853-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e853-102">SYNOPSIS</span></span>
<span data-ttu-id="3e853-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3e853-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="3e853-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e853-104">SYNTAX</span></span>

### <span data-ttu-id="3e853-105">S1</span><span class="sxs-lookup"><span data-stu-id="3e853-105">S1</span></span>
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

### <span data-ttu-id="3e853-106">S2</span><span class="sxs-lookup"><span data-stu-id="3e853-106">S2</span></span>
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

## <span data-ttu-id="3e853-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e853-107">DESCRIPTION</span></span>
<span data-ttu-id="3e853-108">Il cmdlet **set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3e853-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="3e853-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e853-109">EXAMPLES</span></span>

### <span data-ttu-id="3e853-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e853-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="3e853-111">Questo comando modifica il piano Appservice associato a Slot001, nella ContosoWebApp web app associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="3e853-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3e853-112">Usare il collegamento per altre informazioni sulla modifica del piano Appservice e dei vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="3e853-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="3e853-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="3e853-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="3e853-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e853-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="3e853-115">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="3e853-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3e853-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e853-116">PARAMETERS</span></span>

### <span data-ttu-id="3e853-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e853-117">-AppServicePlan</span></span>
<span data-ttu-id="3e853-118">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="3e853-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="3e853-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3e853-119">-AppSettings</span></span>
<span data-ttu-id="3e853-120">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="3e853-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="3e853-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e853-121">-AsJob</span></span>
<span data-ttu-id="3e853-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3e853-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e853-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3e853-123">-AssignIdentity</span></span>
<span data-ttu-id="3e853-124">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="3e853-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="3e853-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3e853-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="3e853-126">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="3e853-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3e853-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="3e853-127">-AzureStoragePath</span></span>
<span data-ttu-id="3e853-128">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="3e853-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="3e853-129">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="3e853-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="3e853-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3e853-130">-ConnectionStrings</span></span>
<span data-ttu-id="3e853-131">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="3e853-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3e853-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="3e853-132">-ContainerImageName</span></span>
<span data-ttu-id="3e853-133">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="3e853-133">Container Image Name</span></span>

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

### <span data-ttu-id="3e853-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="3e853-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="3e853-135">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="3e853-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="3e853-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="3e853-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="3e853-137">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="3e853-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="3e853-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="3e853-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="3e853-139">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="3e853-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="3e853-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3e853-140">-DefaultDocuments</span></span>
<span data-ttu-id="3e853-141">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="3e853-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="3e853-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e853-142">-DefaultProfile</span></span>
<span data-ttu-id="3e853-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e853-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e853-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3e853-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3e853-145">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="3e853-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3e853-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="3e853-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="3e853-147">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="3e853-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="3e853-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3e853-148">-HandlerMappings</span></span>
<span data-ttu-id="3e853-149">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="3e853-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3e853-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3e853-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3e853-151">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="3e853-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3e853-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3e853-152">-HttpsOnly</span></span>
<span data-ttu-id="3e853-153">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="3e853-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="3e853-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3e853-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="3e853-155">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="3e853-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3e853-156">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e853-156">-Name</span></span>
<span data-ttu-id="3e853-157">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="3e853-157">WebApp Name</span></span>

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

### <span data-ttu-id="3e853-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3e853-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="3e853-159">NET Framework</span><span class="sxs-lookup"><span data-stu-id="3e853-159">Net Framework Version</span></span>

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

### <span data-ttu-id="3e853-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3e853-160">-NumberOfWorkers</span></span>
<span data-ttu-id="3e853-161">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="3e853-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3e853-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3e853-162">-PhpVersion</span></span>
<span data-ttu-id="3e853-163">Versione php</span><span class="sxs-lookup"><span data-stu-id="3e853-163">Php Version</span></span>

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

### <span data-ttu-id="3e853-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3e853-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="3e853-165">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="3e853-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="3e853-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e853-166">-ResourceGroupName</span></span>
<span data-ttu-id="3e853-167">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3e853-167">Resource Group Name</span></span>

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

### <span data-ttu-id="3e853-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="3e853-168">-Slot</span></span>
<span data-ttu-id="3e853-169">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="3e853-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3e853-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3e853-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3e853-171">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="3e853-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3e853-172">-Web App</span><span class="sxs-lookup"><span data-stu-id="3e853-172">-WebApp</span></span>
<span data-ttu-id="3e853-173">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="3e853-173">WebApp Object</span></span>

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

### <span data-ttu-id="3e853-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3e853-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="3e853-175">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="3e853-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="3e853-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e853-176">CommonParameters</span></span>
<span data-ttu-id="3e853-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e853-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e853-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e853-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e853-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e853-179">INPUTS</span></span>

### <span data-ttu-id="3e853-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3e853-180">System.Int32</span></span>

### <span data-ttu-id="3e853-181">System. String</span><span class="sxs-lookup"><span data-stu-id="3e853-181">System.String</span></span>

### <span data-ttu-id="3e853-182">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3e853-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3e853-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e853-183">OUTPUTS</span></span>

### <span data-ttu-id="3e853-184">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3e853-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3e853-185">Note</span><span class="sxs-lookup"><span data-stu-id="3e853-185">NOTES</span></span>

## <span data-ttu-id="3e853-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e853-186">RELATED LINKS</span></span>

[<span data-ttu-id="3e853-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="3e853-188">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="3e853-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="3e853-190">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="3e853-191">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="3e853-192">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e853-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="3e853-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e853-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
