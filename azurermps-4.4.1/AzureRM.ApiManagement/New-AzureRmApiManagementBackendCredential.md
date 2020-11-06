---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517223"
---
# <span data-ttu-id="caf84-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="caf84-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="caf84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="caf84-102">SYNOPSIS</span></span>
<span data-ttu-id="caf84-103">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="caf84-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caf84-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caf84-105">DESCRIPTION</span></span>
<span data-ttu-id="caf84-106">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="caf84-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="caf84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caf84-107">EXAMPLES</span></span>

### <span data-ttu-id="caf84-108">Creare un oggetto In-Memory credenziali di backend</span><span class="sxs-lookup"><span data-stu-id="caf84-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="caf84-109">Crea un contratto di credenziali back-end</span><span class="sxs-lookup"><span data-stu-id="caf84-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="caf84-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="caf84-110">PARAMETERS</span></span>

### <span data-ttu-id="caf84-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="caf84-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="caf84-112">Intestazione di autorizzazione usata per il backend.</span><span class="sxs-lookup"><span data-stu-id="caf84-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="caf84-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="caf84-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="caf84-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="caf84-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="caf84-115">Schema di autorizzazione usato per il backend.</span><span class="sxs-lookup"><span data-stu-id="caf84-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="caf84-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="caf84-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="caf84-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="caf84-117">-CertificateThumbprint</span></span>
<span data-ttu-id="caf84-118">Identificazioni personali del certificato client.</span><span class="sxs-lookup"><span data-stu-id="caf84-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="caf84-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="caf84-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf84-120">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="caf84-120">-Header</span></span>
<span data-ttu-id="caf84-121">Valori dei parametri di intestazione accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="caf84-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="caf84-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="caf84-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf84-123">-Query</span><span class="sxs-lookup"><span data-stu-id="caf84-123">-Query</span></span>
<span data-ttu-id="caf84-124">Valori dei parametri di query accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="caf84-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="caf84-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="caf84-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf84-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf84-126">-DefaultProfile</span></span>
<span data-ttu-id="caf84-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caf84-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caf84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf84-128">CommonParameters</span></span>
<span data-ttu-id="caf84-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf84-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf84-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf84-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="caf84-131">INPUTS</span></span>

## <span data-ttu-id="caf84-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caf84-132">OUTPUTS</span></span>

### <span data-ttu-id="caf84-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="caf84-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="caf84-134">Note</span><span class="sxs-lookup"><span data-stu-id="caf84-134">NOTES</span></span>

## <span data-ttu-id="caf84-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caf84-135">RELATED LINKS</span></span>

[<span data-ttu-id="caf84-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="caf84-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="caf84-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="caf84-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="caf84-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="caf84-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="caf84-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="caf84-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="caf84-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="caf84-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
