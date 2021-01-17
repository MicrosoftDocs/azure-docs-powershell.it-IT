---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364976"
---
# <span data-ttu-id="3f627-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3f627-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="3f627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f627-102">SYNOPSIS</span></span>
<span data-ttu-id="3f627-103">Crea un nuovo oggetto proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="3f627-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="3f627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f627-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f627-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f627-105">DESCRIPTION</span></span>
<span data-ttu-id="3f627-106">Crea un nuovo oggetto proxy back-end che può essere inviato tramite pipe durante la creazione di una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="3f627-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="3f627-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f627-107">EXAMPLES</span></span>

### <span data-ttu-id="3f627-108">Esempio 1: creare un proxy back-end In-Memory oggetto</span><span class="sxs-lookup"><span data-stu-id="3f627-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="3f627-109">Crea un oggetto proxy back-end e configura backend</span><span class="sxs-lookup"><span data-stu-id="3f627-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="3f627-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f627-110">PARAMETERS</span></span>

### <span data-ttu-id="3f627-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f627-111">-DefaultProfile</span></span>
<span data-ttu-id="3f627-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f627-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f627-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="3f627-113">-ProxyCredential</span></span>
<span data-ttu-id="3f627-114">Credenziali usate per connettersi al proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="3f627-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="3f627-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3f627-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="3f627-116">-URL</span><span class="sxs-lookup"><span data-stu-id="3f627-116">-Url</span></span>
<span data-ttu-id="3f627-117">URL del server proxy da usare quando si inoltrano le chiamate al backend.</span><span class="sxs-lookup"><span data-stu-id="3f627-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="3f627-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f627-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3f627-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f627-119">CommonParameters</span></span>
<span data-ttu-id="3f627-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f627-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f627-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f627-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f627-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f627-122">INPUTS</span></span>

### <span data-ttu-id="3f627-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f627-123">None</span></span>

## <span data-ttu-id="3f627-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f627-124">OUTPUTS</span></span>

### <span data-ttu-id="3f627-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3f627-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="3f627-126">Note</span><span class="sxs-lookup"><span data-stu-id="3f627-126">NOTES</span></span>

## <span data-ttu-id="3f627-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f627-127">RELATED LINKS</span></span>

[<span data-ttu-id="3f627-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3f627-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="3f627-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3f627-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="3f627-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3f627-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="3f627-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3f627-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="3f627-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3f627-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
