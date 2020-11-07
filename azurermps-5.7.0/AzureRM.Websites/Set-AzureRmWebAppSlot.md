---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 717f355326acc4d169bee1e93d98446fa052a5e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687396"
---
# <span data-ttu-id="ef42b-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ef42b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef42b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef42b-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ef42b-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef42b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef42b-104">SYNTAX</span></span>

### <span data-ttu-id="ef42b-105">S1</span><span class="sxs-lookup"><span data-stu-id="ef42b-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef42b-106">S2</span><span class="sxs-lookup"><span data-stu-id="ef42b-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef42b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef42b-107">DESCRIPTION</span></span>
<span data-ttu-id="ef42b-108">Il cmdlet **set-AzureRmWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ef42b-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="ef42b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef42b-109">EXAMPLES</span></span>

### <span data-ttu-id="ef42b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef42b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="ef42b-111">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ef42b-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ef42b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef42b-112">PARAMETERS</span></span>

### <span data-ttu-id="ef42b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef42b-113">-AppServicePlan</span></span>
<span data-ttu-id="ef42b-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ef42b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="ef42b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ef42b-115">-AppSettings</span></span>
<span data-ttu-id="ef42b-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="ef42b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="ef42b-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ef42b-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="ef42b-118">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="ef42b-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="ef42b-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ef42b-119">-ConnectionStrings</span></span>
<span data-ttu-id="ef42b-120">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="ef42b-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="ef42b-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ef42b-121">-DefaultDocuments</span></span>
<span data-ttu-id="ef42b-122">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="ef42b-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="ef42b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef42b-123">-DefaultProfile</span></span>
<span data-ttu-id="ef42b-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef42b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef42b-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ef42b-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ef42b-126">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="ef42b-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="ef42b-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ef42b-127">-HandlerMappings</span></span>
<span data-ttu-id="ef42b-128">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="ef42b-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="ef42b-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ef42b-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ef42b-130">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ef42b-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="ef42b-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ef42b-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="ef42b-132">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="ef42b-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="ef42b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef42b-133">-Name</span></span>
<span data-ttu-id="ef42b-134">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ef42b-134">WebApp Name</span></span>

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

### <span data-ttu-id="ef42b-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ef42b-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="ef42b-136">NET Framework</span><span class="sxs-lookup"><span data-stu-id="ef42b-136">Net Framework Version</span></span>

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

### <span data-ttu-id="ef42b-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ef42b-137">-NumberOfWorkers</span></span>
<span data-ttu-id="ef42b-138">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="ef42b-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ef42b-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ef42b-139">-PhpVersion</span></span>
<span data-ttu-id="ef42b-140">Versione php</span><span class="sxs-lookup"><span data-stu-id="ef42b-140">Php Version</span></span>

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

### <span data-ttu-id="ef42b-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ef42b-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="ef42b-142">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="ef42b-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="ef42b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef42b-143">-ResourceGroupName</span></span>
<span data-ttu-id="ef42b-144">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ef42b-144">Resource Group Name</span></span>

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

### <span data-ttu-id="ef42b-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="ef42b-145">-Slot</span></span>
<span data-ttu-id="ef42b-146">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ef42b-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ef42b-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ef42b-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ef42b-148">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="ef42b-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="ef42b-149">-Web App</span><span class="sxs-lookup"><span data-stu-id="ef42b-149">-WebApp</span></span>
<span data-ttu-id="ef42b-150">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ef42b-150">WebApp Object</span></span>

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

### <span data-ttu-id="ef42b-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ef42b-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="ef42b-152">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="ef42b-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="ef42b-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef42b-153">-AsJob</span></span>
<span data-ttu-id="ef42b-154">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ef42b-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef42b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef42b-155">CommonParameters</span></span>
<span data-ttu-id="ef42b-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef42b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef42b-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef42b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef42b-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef42b-158">INPUTS</span></span>

### <span data-ttu-id="ef42b-159">Int32</span><span class="sxs-lookup"><span data-stu-id="ef42b-159">Int32</span></span>
<span data-ttu-id="ef42b-160">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ef42b-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="ef42b-161">Sito</span><span class="sxs-lookup"><span data-stu-id="ef42b-161">Site</span></span>
<span data-ttu-id="ef42b-162">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ef42b-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ef42b-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef42b-163">OUTPUTS</span></span>

## <span data-ttu-id="ef42b-164">Note</span><span class="sxs-lookup"><span data-stu-id="ef42b-164">NOTES</span></span>

## <span data-ttu-id="ef42b-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef42b-165">RELATED LINKS</span></span>

[<span data-ttu-id="ef42b-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-167">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-167">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-168">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-168">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-169">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-169">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-170">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-170">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-171">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef42b-171">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ef42b-172">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef42b-172">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
