---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861830"
---
# <span data-ttu-id="06975-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="06975-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06975-102">SYNOPSIS</span></span>
<span data-ttu-id="06975-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="06975-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="06975-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06975-104">SYNTAX</span></span>

### <span data-ttu-id="06975-105">S1</span><span class="sxs-lookup"><span data-stu-id="06975-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06975-106">S2</span><span class="sxs-lookup"><span data-stu-id="06975-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06975-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06975-107">DESCRIPTION</span></span>
<span data-ttu-id="06975-108">Il cmdlet **set-AzWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="06975-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="06975-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06975-109">EXAMPLES</span></span>

### <span data-ttu-id="06975-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06975-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="06975-111">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="06975-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="06975-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06975-112">PARAMETERS</span></span>

### <span data-ttu-id="06975-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="06975-113">-AppServicePlan</span></span>
<span data-ttu-id="06975-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="06975-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="06975-115">-AppSettings</span></span>
<span data-ttu-id="06975-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="06975-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="06975-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="06975-118">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="06975-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="06975-119">-ConnectionStrings</span></span>
<span data-ttu-id="06975-120">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="06975-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="06975-121">-DefaultDocuments</span></span>
<span data-ttu-id="06975-122">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="06975-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06975-123">-DefaultProfile</span></span>
<span data-ttu-id="06975-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06975-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="06975-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="06975-126">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="06975-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="06975-127">-HandlerMappings</span></span>
<span data-ttu-id="06975-128">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="06975-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="06975-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="06975-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="06975-130">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="06975-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="06975-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="06975-132">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="06975-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="06975-133">-Name</span></span>
<span data-ttu-id="06975-134">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="06975-134">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06975-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="06975-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="06975-136">NET Framework</span><span class="sxs-lookup"><span data-stu-id="06975-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="06975-137">-NumberOfWorkers</span></span>
<span data-ttu-id="06975-138">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="06975-138">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06975-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="06975-139">-PhpVersion</span></span>
<span data-ttu-id="06975-140">Versione php</span><span class="sxs-lookup"><span data-stu-id="06975-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="06975-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="06975-142">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="06975-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06975-143">-ResourceGroupName</span></span>
<span data-ttu-id="06975-144">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="06975-144">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="06975-145">-Slot</span></span>
<span data-ttu-id="06975-146">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="06975-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="06975-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="06975-148">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="06975-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-149">-Web App</span><span class="sxs-lookup"><span data-stu-id="06975-149">-WebApp</span></span>
<span data-ttu-id="06975-150">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="06975-150">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06975-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="06975-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="06975-152">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="06975-152">Web Sockets Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="06975-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="06975-153">-HttpsOnly</span></span>
<span data-ttu-id="06975-154">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in uno slot esistente</span><span class="sxs-lookup"><span data-stu-id="06975-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="06975-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="06975-155">-AssignIdentity</span></span>
<span data-ttu-id="06975-156">Abilitare/disabilitare MSI in uno slot esistente [Anteprima]</span><span class="sxs-lookup"><span data-stu-id="06975-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06975-157">-AsJob</span></span>
<span data-ttu-id="06975-158">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="06975-158">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06975-159">CommonParameters</span></span>
<span data-ttu-id="06975-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06975-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06975-161">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06975-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06975-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06975-162">INPUTS</span></span>

### <span data-ttu-id="06975-163">Int32</span><span class="sxs-lookup"><span data-stu-id="06975-163">Int32</span></span>
<span data-ttu-id="06975-164">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="06975-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="06975-165">Sito</span><span class="sxs-lookup"><span data-stu-id="06975-165">Site</span></span>
<span data-ttu-id="06975-166">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="06975-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="06975-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06975-167">OUTPUTS</span></span>

## <span data-ttu-id="06975-168">Note</span><span class="sxs-lookup"><span data-stu-id="06975-168">NOTES</span></span>

## <span data-ttu-id="06975-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06975-169">RELATED LINKS</span></span>

[<span data-ttu-id="06975-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="06975-171">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="06975-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="06975-173">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="06975-174">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="06975-175">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="06975-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="06975-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="06975-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
