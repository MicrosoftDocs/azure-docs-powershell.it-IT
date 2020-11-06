---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513976"
---
# <span data-ttu-id="22a02-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22a02-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="22a02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22a02-102">SYNOPSIS</span></span>
<span data-ttu-id="22a02-103">Modifica un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="22a02-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22a02-104">SYNTAX</span></span>

### <span data-ttu-id="22a02-105">EventHubLoggerSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22a02-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a02-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="22a02-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22a02-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22a02-107">DESCRIPTION</span></span>
<span data-ttu-id="22a02-108">Il cmdlet **set-AzureRmApiManagementLogger** modifica le impostazioni di un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="22a02-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="22a02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22a02-109">EXAMPLES</span></span>

### <span data-ttu-id="22a02-110">Esempio 1: modificare il logger di EventHub</span><span class="sxs-lookup"><span data-stu-id="22a02-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="22a02-111">Questo comando modifica un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="22a02-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="22a02-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22a02-112">PARAMETERS</span></span>

### <span data-ttu-id="22a02-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="22a02-113">-ConnectionString</span></span>
<span data-ttu-id="22a02-114">Specifica una stringa di connessione hub eventi di Azure che include i diritti di invio dei criteri.</span><span class="sxs-lookup"><span data-stu-id="22a02-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="22a02-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="22a02-115">-Context</span></span>
<span data-ttu-id="22a02-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="22a02-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a02-117">-DefaultProfile</span></span>
<span data-ttu-id="22a02-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22a02-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a02-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="22a02-119">-Description</span></span>
<span data-ttu-id="22a02-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="22a02-120">Specifies a description.</span></span>

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

### <span data-ttu-id="22a02-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="22a02-121">-InstrumentationKey</span></span>
<span data-ttu-id="22a02-122">Chiave di strumentazione degli approfondimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22a02-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="22a02-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="22a02-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="22a02-124">-Buffered</span><span class="sxs-lookup"><span data-stu-id="22a02-124">-IsBuffered</span></span>
<span data-ttu-id="22a02-125">Specifica che i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="22a02-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="22a02-126">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="22a02-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="22a02-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="22a02-127">-LoggerId</span></span>
<span data-ttu-id="22a02-128">Specifica l'ID del logger da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="22a02-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="22a02-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="22a02-129">-Name</span></span>
<span data-ttu-id="22a02-130">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="22a02-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="22a02-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22a02-131">-PassThru</span></span>
<span data-ttu-id="22a02-132">Indica che questo cmdlet restituisce il  **PsApiManagementLogger** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22a02-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22a02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a02-133">CommonParameters</span></span>
<span data-ttu-id="22a02-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a02-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a02-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22a02-136">INPUTS</span></span>

### <span data-ttu-id="22a02-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22a02-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22a02-138">System. String</span><span class="sxs-lookup"><span data-stu-id="22a02-138">System.String</span></span>

### <span data-ttu-id="22a02-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22a02-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22a02-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22a02-140">OUTPUTS</span></span>

### <span data-ttu-id="22a02-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22a02-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="22a02-142">Note</span><span class="sxs-lookup"><span data-stu-id="22a02-142">NOTES</span></span>

## <span data-ttu-id="22a02-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22a02-143">RELATED LINKS</span></span>

[<span data-ttu-id="22a02-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22a02-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="22a02-145">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22a02-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="22a02-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22a02-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


