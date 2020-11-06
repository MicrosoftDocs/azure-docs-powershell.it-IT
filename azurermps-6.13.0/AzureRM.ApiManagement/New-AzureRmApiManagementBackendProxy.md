---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512040"
---
# <span data-ttu-id="52bff-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="52bff-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="52bff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52bff-102">SYNOPSIS</span></span>
<span data-ttu-id="52bff-103">Crea un nuovo oggetto proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="52bff-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52bff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52bff-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52bff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52bff-105">DESCRIPTION</span></span>
<span data-ttu-id="52bff-106">Crea un nuovo oggetto proxy back-end che può essere inviato tramite pipe durante la creazione di una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="52bff-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="52bff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52bff-107">EXAMPLES</span></span>

### <span data-ttu-id="52bff-108">Creare un proxy back-end In-Memory oggetto</span><span class="sxs-lookup"><span data-stu-id="52bff-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="52bff-109">Crea un oggetto proxy back-end e configura backend</span><span class="sxs-lookup"><span data-stu-id="52bff-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="52bff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52bff-110">PARAMETERS</span></span>

### <span data-ttu-id="52bff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bff-111">-DefaultProfile</span></span>
<span data-ttu-id="52bff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52bff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52bff-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="52bff-113">-ProxyCredential</span></span>
<span data-ttu-id="52bff-114">Credenziali usate per connettersi al proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="52bff-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="52bff-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="52bff-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bff-116">-URL</span><span class="sxs-lookup"><span data-stu-id="52bff-116">-Url</span></span>
<span data-ttu-id="52bff-117">URL del server proxy da usare quando si inoltrano le chiamate al backend.</span><span class="sxs-lookup"><span data-stu-id="52bff-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="52bff-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="52bff-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bff-119">CommonParameters</span></span>
<span data-ttu-id="52bff-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52bff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bff-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52bff-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bff-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52bff-122">INPUTS</span></span>

### <span data-ttu-id="52bff-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="52bff-123">None</span></span>

## <span data-ttu-id="52bff-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52bff-124">OUTPUTS</span></span>

### <span data-ttu-id="52bff-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="52bff-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="52bff-126">Note</span><span class="sxs-lookup"><span data-stu-id="52bff-126">NOTES</span></span>

## <span data-ttu-id="52bff-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52bff-127">RELATED LINKS</span></span>

[<span data-ttu-id="52bff-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52bff-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="52bff-129">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52bff-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="52bff-130">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="52bff-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="52bff-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52bff-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="52bff-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52bff-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
