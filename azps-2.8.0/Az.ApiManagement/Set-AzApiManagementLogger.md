---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 8f1931cb5e73e3850cd011c16d327f8e8abc3a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675892"
---
# <span data-ttu-id="7a47c-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7a47c-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="7a47c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a47c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a47c-103">Modifica un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="7a47c-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="7a47c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a47c-104">SYNTAX</span></span>

### <span data-ttu-id="7a47c-105">EventHubLoggerSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a47c-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a47c-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="7a47c-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a47c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a47c-107">DESCRIPTION</span></span>
<span data-ttu-id="7a47c-108">Il cmdlet **set-AzApiManagementLogger** modifica le impostazioni di un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a47c-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="7a47c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a47c-109">EXAMPLES</span></span>

### <span data-ttu-id="7a47c-110">Esempio 1: modificare il logger di EventHub</span><span class="sxs-lookup"><span data-stu-id="7a47c-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="7a47c-111">Questo comando modifica un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="7a47c-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="7a47c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a47c-112">PARAMETERS</span></span>

### <span data-ttu-id="7a47c-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7a47c-113">-ConnectionString</span></span>
<span data-ttu-id="7a47c-114">Specifica una stringa di connessione hub eventi di Azure che include i diritti di invio dei criteri.</span><span class="sxs-lookup"><span data-stu-id="7a47c-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7a47c-115">-Context</span></span>
<span data-ttu-id="7a47c-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7a47c-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a47c-117">-DefaultProfile</span></span>
<span data-ttu-id="7a47c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a47c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a47c-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a47c-119">-Description</span></span>
<span data-ttu-id="7a47c-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="7a47c-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="7a47c-121">-InstrumentationKey</span></span>
<span data-ttu-id="7a47c-122">Chiave di strumentazione degli approfondimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7a47c-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="7a47c-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7a47c-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-124">-Buffered</span><span class="sxs-lookup"><span data-stu-id="7a47c-124">-IsBuffered</span></span>
<span data-ttu-id="7a47c-125">Specifica che i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7a47c-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="7a47c-126">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="7a47c-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="7a47c-127">-LoggerId</span></span>
<span data-ttu-id="7a47c-128">Specifica l'ID del logger da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7a47c-128">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a47c-129">-Name</span></span>
<span data-ttu-id="7a47c-130">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="7a47c-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a47c-131">-PassThru</span></span>
<span data-ttu-id="7a47c-132">Indica che questo cmdlet restituisce il  **PsApiManagementLogger** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a47c-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a47c-133">-Confirm</span></span>
<span data-ttu-id="7a47c-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a47c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a47c-135">-WhatIf</span></span>
<span data-ttu-id="7a47c-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a47c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a47c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a47c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a47c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a47c-138">CommonParameters</span></span>
<span data-ttu-id="7a47c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a47c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a47c-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a47c-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a47c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a47c-141">INPUTS</span></span>

### <span data-ttu-id="7a47c-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a47c-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a47c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a47c-143">System.String</span></span>

### <span data-ttu-id="7a47c-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a47c-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a47c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a47c-145">OUTPUTS</span></span>

### <span data-ttu-id="7a47c-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7a47c-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="7a47c-147">Note</span><span class="sxs-lookup"><span data-stu-id="7a47c-147">NOTES</span></span>

## <span data-ttu-id="7a47c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a47c-148">RELATED LINKS</span></span>

[<span data-ttu-id="7a47c-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7a47c-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="7a47c-150">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7a47c-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="7a47c-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7a47c-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


