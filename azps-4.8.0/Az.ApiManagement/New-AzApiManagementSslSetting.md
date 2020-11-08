---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191723"
---
# <span data-ttu-id="53fba-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="53fba-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="53fba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53fba-102">SYNOPSIS</span></span>
<span data-ttu-id="53fba-103">Crea un'istanza di PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="53fba-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="53fba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53fba-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53fba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53fba-105">DESCRIPTION</span></span>
<span data-ttu-id="53fba-106">Comando helper per creare un'istanza di PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="53fba-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="53fba-107">Questo comando deve essere usato con il comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53fba-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="53fba-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53fba-108">EXAMPLES</span></span>

### <span data-ttu-id="53fba-109">Esempio 1: creare un'impostazione SSL per abilitare TLS 1,0 sia in backend che in frontend</span><span class="sxs-lookup"><span data-stu-id="53fba-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="53fba-110">Crea una nuova istanza di PsApiManagementSslSetting per abilitare TLSv 1,0 sia in frontend (tra client e APIM) che in backend (tra APIM e backend) del gateway di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53fba-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="53fba-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53fba-111">PARAMETERS</span></span>

### <span data-ttu-id="53fba-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="53fba-112">-BackendProtocol</span></span>
<span data-ttu-id="53fba-113">Impostazioni del protocollo di sicurezza back-end.</span><span class="sxs-lookup"><span data-stu-id="53fba-113">Backend Security protocol settings.</span></span> <span data-ttu-id="53fba-114">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="53fba-114">This parameter is optional.</span></span>
<span data-ttu-id="53fba-115">Le impostazioni valide per il protocollo sono `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="53fba-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="53fba-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="53fba-116">-CipherSuite</span></span>
<span data-ttu-id="53fba-117">Impostazioni delle suite crittografiche SSL nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="53fba-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="53fba-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="53fba-118">This parameter is optional.</span></span>
<span data-ttu-id="53fba-119">Le impostazioni valide sono `TripleDes168` -Abilita/Disabilita trippa Des 168</span><span class="sxs-lookup"><span data-stu-id="53fba-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="53fba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53fba-120">-DefaultProfile</span></span>
<span data-ttu-id="53fba-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53fba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53fba-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="53fba-122">-FrontendProtocol</span></span>
<span data-ttu-id="53fba-123">Impostazioni protocolli di sicurezza frontend.</span><span class="sxs-lookup"><span data-stu-id="53fba-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="53fba-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="53fba-124">This parameter is optional.</span></span>
<span data-ttu-id="53fba-125">Le impostazioni valide per il protocollo sono `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="53fba-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="53fba-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="53fba-126">-ServerProtocol</span></span>
<span data-ttu-id="53fba-127">Impostazioni del protocollo server come Http2.</span><span class="sxs-lookup"><span data-stu-id="53fba-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="53fba-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="53fba-128">This parameter is optional.</span></span>
<span data-ttu-id="53fba-129">Le impostazioni valide sono `Http2` -Enable Http 2,0</span><span class="sxs-lookup"><span data-stu-id="53fba-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="53fba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fba-130">CommonParameters</span></span>
<span data-ttu-id="53fba-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53fba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fba-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53fba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fba-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53fba-133">INPUTS</span></span>

### <span data-ttu-id="53fba-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="53fba-134">None</span></span>

## <span data-ttu-id="53fba-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53fba-135">OUTPUTS</span></span>

### <span data-ttu-id="53fba-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="53fba-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="53fba-137">Note</span><span class="sxs-lookup"><span data-stu-id="53fba-137">NOTES</span></span>

## <span data-ttu-id="53fba-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53fba-138">RELATED LINKS</span></span>

[<span data-ttu-id="53fba-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="53fba-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

