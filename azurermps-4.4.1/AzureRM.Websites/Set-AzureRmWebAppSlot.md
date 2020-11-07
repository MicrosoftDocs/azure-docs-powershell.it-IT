---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685510"
---
# <span data-ttu-id="0140a-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="0140a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0140a-102">SYNOPSIS</span></span>
<span data-ttu-id="0140a-103">Modifica uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0140a-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0140a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0140a-104">SYNTAX</span></span>

### <span data-ttu-id="0140a-105">S1</span><span class="sxs-lookup"><span data-stu-id="0140a-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0140a-106">S2</span><span class="sxs-lookup"><span data-stu-id="0140a-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0140a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0140a-107">DESCRIPTION</span></span>
<span data-ttu-id="0140a-108">Il cmdlet **set-AzureRmWebApp** imposta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0140a-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="0140a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0140a-109">EXAMPLES</span></span>

### <span data-ttu-id="0140a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0140a-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="0140a-111">Questo comando imposta HttpLoggingEnabled su true per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="0140a-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0140a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0140a-112">PARAMETERS</span></span>

### <span data-ttu-id="0140a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0140a-113">-AppServicePlan</span></span>
<span data-ttu-id="0140a-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="0140a-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="0140a-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0140a-115">-AppSettings</span></span>
<span data-ttu-id="0140a-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="0140a-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="0140a-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0140a-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="0140a-118">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="0140a-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="0140a-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0140a-119">-ConnectionStrings</span></span>
<span data-ttu-id="0140a-120">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="0140a-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="0140a-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0140a-121">-DefaultDocuments</span></span>
<span data-ttu-id="0140a-122">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="0140a-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="0140a-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0140a-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0140a-124">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="0140a-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="0140a-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0140a-125">-HandlerMappings</span></span>
<span data-ttu-id="0140a-126">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="0140a-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="0140a-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0140a-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0140a-128">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="0140a-128">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="0140a-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0140a-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="0140a-130">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="0140a-130">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="0140a-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0140a-131">-Name</span></span>
<span data-ttu-id="0140a-132">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="0140a-132">WebApp Name</span></span>

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

### <span data-ttu-id="0140a-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0140a-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="0140a-134">NET Framework</span><span class="sxs-lookup"><span data-stu-id="0140a-134">Net Framework Version</span></span>

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

### <span data-ttu-id="0140a-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0140a-135">-NumberOfWorkers</span></span>
<span data-ttu-id="0140a-136">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="0140a-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="0140a-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0140a-137">-PhpVersion</span></span>
<span data-ttu-id="0140a-138">Versione php</span><span class="sxs-lookup"><span data-stu-id="0140a-138">Php Version</span></span>

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

### <span data-ttu-id="0140a-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0140a-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="0140a-140">Booleano abilitato per l'analisi delle richieste</span><span class="sxs-lookup"><span data-stu-id="0140a-140">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="0140a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0140a-141">-ResourceGroupName</span></span>
<span data-ttu-id="0140a-142">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0140a-142">Resource Group Name</span></span>

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

### <span data-ttu-id="0140a-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="0140a-143">-Slot</span></span>
<span data-ttu-id="0140a-144">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="0140a-144">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0140a-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0140a-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0140a-146">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="0140a-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="0140a-147">-Web App</span><span class="sxs-lookup"><span data-stu-id="0140a-147">-WebApp</span></span>
<span data-ttu-id="0140a-148">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="0140a-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0140a-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0140a-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="0140a-150">Socket Web abilitati Boolean</span><span class="sxs-lookup"><span data-stu-id="0140a-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="0140a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0140a-151">-DefaultProfile</span></span>
<span data-ttu-id="0140a-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0140a-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0140a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0140a-153">CommonParameters</span></span>
<span data-ttu-id="0140a-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0140a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0140a-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0140a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0140a-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0140a-156">INPUTS</span></span>

### <span data-ttu-id="0140a-157">Int32</span><span class="sxs-lookup"><span data-stu-id="0140a-157">Int32</span></span>
<span data-ttu-id="0140a-158">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0140a-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="0140a-159">Sito</span><span class="sxs-lookup"><span data-stu-id="0140a-159">Site</span></span>
<span data-ttu-id="0140a-160">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0140a-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0140a-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0140a-161">OUTPUTS</span></span>

## <span data-ttu-id="0140a-162">Note</span><span class="sxs-lookup"><span data-stu-id="0140a-162">NOTES</span></span>

## <span data-ttu-id="0140a-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0140a-163">RELATED LINKS</span></span>

[<span data-ttu-id="0140a-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-165">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-166">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-167">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-168">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-169">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0140a-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="0140a-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0140a-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
