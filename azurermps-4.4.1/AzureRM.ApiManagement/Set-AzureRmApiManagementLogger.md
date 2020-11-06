---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518431"
---
# <span data-ttu-id="04254-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="04254-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="04254-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04254-102">SYNOPSIS</span></span>
<span data-ttu-id="04254-103">Modifica un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="04254-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04254-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04254-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04254-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04254-105">DESCRIPTION</span></span>
<span data-ttu-id="04254-106">Il cmdlet **set-AzureRmApiManagementLogger** modifica le impostazioni di un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="04254-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="04254-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04254-107">EXAMPLES</span></span>

### <span data-ttu-id="04254-108">Esempio 1: modificare un logger</span><span class="sxs-lookup"><span data-stu-id="04254-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="04254-109">Questo comando modifica un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="04254-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="04254-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04254-110">PARAMETERS</span></span>

### <span data-ttu-id="04254-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="04254-111">-ConnectionString</span></span>
<span data-ttu-id="04254-112">Specifica una stringa di connessione hub eventi di Azure che include i diritti di invio dei criteri.</span><span class="sxs-lookup"><span data-stu-id="04254-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="04254-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="04254-113">-Context</span></span>
<span data-ttu-id="04254-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="04254-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="04254-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="04254-115">-Description</span></span>
<span data-ttu-id="04254-116">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="04254-116">Specifies a description.</span></span>

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

### <span data-ttu-id="04254-117">-Buffered</span><span class="sxs-lookup"><span data-stu-id="04254-117">-IsBuffered</span></span>
<span data-ttu-id="04254-118">Specifica che i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="04254-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="04254-119">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="04254-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="04254-120">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="04254-120">-LoggerId</span></span>
<span data-ttu-id="04254-121">Specifica l'ID del logger da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="04254-121">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="04254-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="04254-122">-Name</span></span>
<span data-ttu-id="04254-123">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="04254-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="04254-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04254-124">-PassThru</span></span>
<span data-ttu-id="04254-125">Indica che questo cmdlet restituisce il  **PsApiManagementLogger** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04254-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="04254-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04254-126">-DefaultProfile</span></span>
<span data-ttu-id="04254-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04254-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04254-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04254-128">CommonParameters</span></span>
<span data-ttu-id="04254-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04254-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04254-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04254-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04254-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04254-131">INPUTS</span></span>

## <span data-ttu-id="04254-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04254-132">OUTPUTS</span></span>

### <span data-ttu-id="04254-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="04254-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="04254-134">Note</span><span class="sxs-lookup"><span data-stu-id="04254-134">NOTES</span></span>

## <span data-ttu-id="04254-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04254-135">RELATED LINKS</span></span>

[<span data-ttu-id="04254-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="04254-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="04254-137">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="04254-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="04254-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="04254-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


