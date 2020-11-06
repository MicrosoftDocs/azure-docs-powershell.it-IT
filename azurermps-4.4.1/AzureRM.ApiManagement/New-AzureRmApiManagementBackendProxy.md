---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517215"
---
# <span data-ttu-id="ac1f5-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ac1f5-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="ac1f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1f5-103">Crea un nuovo oggetto proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac1f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac1f5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac1f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1f5-106">Crea un nuovo oggetto proxy back-end che può essere inviato tramite pipe durante la creazione di una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="ac1f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac1f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ac1f5-108">Creare un proxy back-end In-Memory oggetto</span><span class="sxs-lookup"><span data-stu-id="ac1f5-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="ac1f5-109">Crea un oggetto proxy back-end</span><span class="sxs-lookup"><span data-stu-id="ac1f5-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="ac1f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac1f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ac1f5-111">-Password</span><span class="sxs-lookup"><span data-stu-id="ac1f5-111">-Password</span></span>
<span data-ttu-id="ac1f5-112">Password proxy usata per la connessione al proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="ac1f5-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="ac1f5-114">-URL</span><span class="sxs-lookup"><span data-stu-id="ac1f5-114">-Url</span></span>
<span data-ttu-id="ac1f5-115">URL del server proxy da usare quando si inoltrano le chiamate al backend.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="ac1f5-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ac1f5-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="ac1f5-117">-UserName</span></span>
<span data-ttu-id="ac1f5-118">Nome utente proxy usato per la connessione al proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="ac1f5-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ac1f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1f5-120">-DefaultProfile</span></span>
<span data-ttu-id="ac1f5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac1f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1f5-122">CommonParameters</span></span>
<span data-ttu-id="ac1f5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1f5-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1f5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1f5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac1f5-125">INPUTS</span></span>

## <span data-ttu-id="ac1f5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac1f5-126">OUTPUTS</span></span>

### <span data-ttu-id="ac1f5-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ac1f5-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="ac1f5-128">Note</span><span class="sxs-lookup"><span data-stu-id="ac1f5-128">NOTES</span></span>

## <span data-ttu-id="ac1f5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac1f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac1f5-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac1f5-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ac1f5-131">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac1f5-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ac1f5-132">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ac1f5-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="ac1f5-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac1f5-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ac1f5-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac1f5-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
