---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516292"
---
# <span data-ttu-id="edd1c-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="edd1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="edd1c-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="edd1c-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edd1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edd1c-104">SYNTAX</span></span>

### <span data-ttu-id="edd1c-105">S1</span><span class="sxs-lookup"><span data-stu-id="edd1c-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edd1c-106">S2</span><span class="sxs-lookup"><span data-stu-id="edd1c-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edd1c-107">DESCRIPTION</span></span>
<span data-ttu-id="edd1c-108">Il cmdlet **set-AzureRmWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="edd1c-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="edd1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edd1c-109">EXAMPLES</span></span>

### <span data-ttu-id="edd1c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edd1c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="edd1c-111">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="edd1c-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="edd1c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edd1c-112">PARAMETERS</span></span>

### <span data-ttu-id="edd1c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="edd1c-113">-AppServicePlan</span></span>
<span data-ttu-id="edd1c-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="edd1c-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="edd1c-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="edd1c-115">-AppSettings</span></span>
<span data-ttu-id="edd1c-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="edd1c-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="edd1c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edd1c-117">-AsJob</span></span>
<span data-ttu-id="edd1c-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="edd1c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edd1c-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="edd1c-119">-AssignIdentity</span></span>
<span data-ttu-id="edd1c-120">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="edd1c-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="edd1c-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="edd1c-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="edd1c-122">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="edd1c-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="edd1c-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="edd1c-123">-ConnectionStrings</span></span>
<span data-ttu-id="edd1c-124">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="edd1c-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="edd1c-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="edd1c-125">-ContainerImageName</span></span>
<span data-ttu-id="edd1c-126">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="edd1c-126">Container Image Name</span></span>

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

### <span data-ttu-id="edd1c-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="edd1c-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="edd1c-128">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="edd1c-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="edd1c-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="edd1c-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="edd1c-130">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="edd1c-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="edd1c-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="edd1c-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="edd1c-132">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="edd1c-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="edd1c-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="edd1c-133">-DefaultDocuments</span></span>
<span data-ttu-id="edd1c-134">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="edd1c-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="edd1c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd1c-135">-DefaultProfile</span></span>
<span data-ttu-id="edd1c-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edd1c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd1c-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="edd1c-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="edd1c-138">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="edd1c-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="edd1c-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="edd1c-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="edd1c-140">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="edd1c-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="edd1c-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="edd1c-141">-HandlerMappings</span></span>
<span data-ttu-id="edd1c-142">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="edd1c-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="edd1c-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="edd1c-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="edd1c-144">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="edd1c-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="edd1c-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="edd1c-145">-HttpsOnly</span></span>
<span data-ttu-id="edd1c-146">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="edd1c-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="edd1c-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="edd1c-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="edd1c-148">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="edd1c-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="edd1c-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="edd1c-149">-Name</span></span>
<span data-ttu-id="edd1c-150">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="edd1c-150">WebApp Name</span></span>

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

### <span data-ttu-id="edd1c-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="edd1c-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="edd1c-152">NET Framework</span><span class="sxs-lookup"><span data-stu-id="edd1c-152">Net Framework Version</span></span>

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

### <span data-ttu-id="edd1c-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="edd1c-153">-NumberOfWorkers</span></span>
<span data-ttu-id="edd1c-154">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="edd1c-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="edd1c-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="edd1c-155">-PhpVersion</span></span>
<span data-ttu-id="edd1c-156">Versione php</span><span class="sxs-lookup"><span data-stu-id="edd1c-156">Php Version</span></span>

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

### <span data-ttu-id="edd1c-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="edd1c-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="edd1c-158">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="edd1c-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="edd1c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd1c-159">-ResourceGroupName</span></span>
<span data-ttu-id="edd1c-160">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="edd1c-160">Resource Group Name</span></span>

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

### <span data-ttu-id="edd1c-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="edd1c-161">-Slot</span></span>
<span data-ttu-id="edd1c-162">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="edd1c-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="edd1c-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="edd1c-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="edd1c-164">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="edd1c-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="edd1c-165">-Web App</span><span class="sxs-lookup"><span data-stu-id="edd1c-165">-WebApp</span></span>
<span data-ttu-id="edd1c-166">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="edd1c-166">WebApp Object</span></span>

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

### <span data-ttu-id="edd1c-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="edd1c-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="edd1c-168">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="edd1c-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="edd1c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd1c-169">CommonParameters</span></span>
<span data-ttu-id="edd1c-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd1c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd1c-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd1c-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd1c-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edd1c-172">INPUTS</span></span>

### <span data-ttu-id="edd1c-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="edd1c-173">System.Int32</span></span>
<span data-ttu-id="edd1c-174">Parametri: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="edd1c-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="edd1c-175">System. String</span><span class="sxs-lookup"><span data-stu-id="edd1c-175">System.String</span></span>

### <span data-ttu-id="edd1c-176">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="edd1c-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="edd1c-177">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="edd1c-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="edd1c-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edd1c-178">OUTPUTS</span></span>

### <span data-ttu-id="edd1c-179">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="edd1c-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="edd1c-180">Note</span><span class="sxs-lookup"><span data-stu-id="edd1c-180">NOTES</span></span>

## <span data-ttu-id="edd1c-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edd1c-181">RELATED LINKS</span></span>

[<span data-ttu-id="edd1c-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-183">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-185">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-186">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-187">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edd1c-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="edd1c-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="edd1c-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
