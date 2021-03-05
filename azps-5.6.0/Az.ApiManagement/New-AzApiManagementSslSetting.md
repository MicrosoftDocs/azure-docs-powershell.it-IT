---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001997"
---
# <span data-ttu-id="c4a0b-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="c4a0b-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="c4a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a0b-103">Crea un'istanza di PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="c4a0b-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="c4a0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4a0b-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4a0b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a0b-106">Comando helper per creare un'istanza di PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="c4a0b-107">Questo comando deve essere usato con New-AzApiManagement comando.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="c4a0b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4a0b-108">EXAMPLES</span></span>

### <span data-ttu-id="c4a0b-109">Esempio 1: Creare un'impostazione SSL per abilitare TLS 1.0 sia in Backend che frontend</span><span class="sxs-lookup"><span data-stu-id="c4a0b-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="c4a0b-110">Creare una nuova istanza di PsApiManagementSslSetting per abilitare TLSv 1.0 sia in Frontend (tra client che APIM) e Backend (tra APIM e Backend) di ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="c4a0b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4a0b-111">PARAMETERS</span></span>

### <span data-ttu-id="c4a0b-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="c4a0b-112">-BackendProtocol</span></span>
<span data-ttu-id="c4a0b-113">Impostazioni del protocollo di sicurezza back-end.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-113">Backend Security protocol settings.</span></span> <span data-ttu-id="c4a0b-114">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-114">This parameter is optional.</span></span>
<span data-ttu-id="c4a0b-115">Le impostazioni del protocollo valide sono `Tls11` Tls 1.1 `Tls10` - Tls 1.0 - SSL `Ssl30` 3.0</span><span class="sxs-lookup"><span data-stu-id="c4a0b-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="c4a0b-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c4a0b-116">-CipherSuite</span></span>
<span data-ttu-id="c4a0b-117">Impostazioni dei pacchetti di crittografia Ssl nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="c4a0b-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-118">This parameter is optional.</span></span>
<span data-ttu-id="c4a0b-119">Le impostazioni valide sono `TripleDes168` - Abilitare/Disabilitare Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="c4a0b-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="c4a0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a0b-120">-DefaultProfile</span></span>
<span data-ttu-id="c4a0b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a0b-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="c4a0b-122">-FrontendProtocol</span></span>
<span data-ttu-id="c4a0b-123">Impostazioni dei protocolli di sicurezza frontend.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="c4a0b-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-124">This parameter is optional.</span></span>
<span data-ttu-id="c4a0b-125">Le impostazioni del protocollo valide sono `Tls11` Tls 1.1 `Tls10` - Tls 1.0 - SSL `Ssl30` 3.0</span><span class="sxs-lookup"><span data-stu-id="c4a0b-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="c4a0b-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="c4a0b-126">-ServerProtocol</span></span>
<span data-ttu-id="c4a0b-127">Impostazioni del protocollo server come Http2.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="c4a0b-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-128">This parameter is optional.</span></span>
<span data-ttu-id="c4a0b-129">Le impostazioni valide sono `Http2` - Abilitare Http 2.0</span><span class="sxs-lookup"><span data-stu-id="c4a0b-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="c4a0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a0b-130">CommonParameters</span></span>
<span data-ttu-id="c4a0b-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a0b-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4a0b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a0b-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4a0b-133">INPUTS</span></span>

### <span data-ttu-id="c4a0b-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c4a0b-134">None</span></span>

## <span data-ttu-id="c4a0b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4a0b-135">OUTPUTS</span></span>

### <span data-ttu-id="c4a0b-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="c4a0b-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="c4a0b-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4a0b-137">NOTES</span></span>

## <span data-ttu-id="c4a0b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4a0b-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4a0b-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4a0b-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

