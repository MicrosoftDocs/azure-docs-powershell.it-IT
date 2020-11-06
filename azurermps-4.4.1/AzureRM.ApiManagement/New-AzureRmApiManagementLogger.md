---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517199"
---
# <span data-ttu-id="57be4-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="57be4-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="57be4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57be4-102">SYNOPSIS</span></span>
<span data-ttu-id="57be4-103">Crea un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="57be4-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57be4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57be4-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57be4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57be4-105">DESCRIPTION</span></span>
<span data-ttu-id="57be4-106">Il cmdlet **New-AzureRmApiManagementLogger** crea un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="57be4-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="57be4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57be4-107">EXAMPLES</span></span>

### <span data-ttu-id="57be4-108">Esempio 1: creare un logger</span><span class="sxs-lookup"><span data-stu-id="57be4-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="57be4-109">Questo comando crea un logger denominato ContosoSdkEventHub usando la stringa di connessione specificata.</span><span class="sxs-lookup"><span data-stu-id="57be4-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="57be4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57be4-110">PARAMETERS</span></span>

### <span data-ttu-id="57be4-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="57be4-111">-ConnectionString</span></span>
<span data-ttu-id="57be4-112">Specifica una stringa di connessione hub eventi di Azure che inizia con le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57be4-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="57be4-113">La chiave con i diritti di invio nella stringa di connessione deve essere configurata.</span><span class="sxs-lookup"><span data-stu-id="57be4-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="57be4-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="57be4-114">-Context</span></span>
<span data-ttu-id="57be4-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="57be4-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="57be4-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="57be4-116">-Description</span></span>
<span data-ttu-id="57be4-117">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="57be4-117">Specifies a description.</span></span>

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

### <span data-ttu-id="57be4-118">-Buffered</span><span class="sxs-lookup"><span data-stu-id="57be4-118">-IsBuffered</span></span>
<span data-ttu-id="57be4-119">Specifica se i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="57be4-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="57be4-120">Il valore predefinito è $True.</span><span class="sxs-lookup"><span data-stu-id="57be4-120">The default value is $True.</span></span>
<span data-ttu-id="57be4-121">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="57be4-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57be4-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="57be4-122">-LoggerId</span></span>
<span data-ttu-id="57be4-123">Specifica un ID per il logger.</span><span class="sxs-lookup"><span data-stu-id="57be4-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="57be4-124">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="57be4-124">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="57be4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="57be4-125">-Name</span></span>
<span data-ttu-id="57be4-126">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="57be4-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="57be4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57be4-127">-DefaultProfile</span></span>
<span data-ttu-id="57be4-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57be4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57be4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57be4-129">CommonParameters</span></span>
<span data-ttu-id="57be4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57be4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57be4-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57be4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57be4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57be4-132">INPUTS</span></span>

## <span data-ttu-id="57be4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57be4-133">OUTPUTS</span></span>

### <span data-ttu-id="57be4-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="57be4-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="57be4-135">Note</span><span class="sxs-lookup"><span data-stu-id="57be4-135">NOTES</span></span>

## <span data-ttu-id="57be4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57be4-136">RELATED LINKS</span></span>

[<span data-ttu-id="57be4-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="57be4-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="57be4-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="57be4-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="57be4-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="57be4-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


