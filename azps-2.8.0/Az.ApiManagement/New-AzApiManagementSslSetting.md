---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675981"
---
# <span data-ttu-id="2ded9-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="2ded9-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="2ded9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ded9-102">SYNOPSIS</span></span>
<span data-ttu-id="2ded9-103">Crea un'istanza di PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="2ded9-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="2ded9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ded9-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ded9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ded9-105">DESCRIPTION</span></span>
<span data-ttu-id="2ded9-106">Comando helper per creare un'istanza di PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="2ded9-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="2ded9-107">Questo comando deve essere usato con il comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2ded9-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="2ded9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ded9-108">EXAMPLES</span></span>

### <span data-ttu-id="2ded9-109">Esempio 1: creare un'impostazione SSL per abilitare TLS 1,0 sia in backend che in frontend</span><span class="sxs-lookup"><span data-stu-id="2ded9-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="2ded9-110">Crea una nuova istanza di PsApiManagementSslSetting per abilitare TLSv 1,0 sia in frontend (tra client e APIM) che in backend (tra APIM e backend) del gateway di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2ded9-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="2ded9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ded9-111">PARAMETERS</span></span>

### <span data-ttu-id="2ded9-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="2ded9-112">-BackendProtocol</span></span>
<span data-ttu-id="2ded9-113">Impostazioni del protocollo di sicurezza back-end.</span><span class="sxs-lookup"><span data-stu-id="2ded9-113">Backend Security protocol settings.</span></span> <span data-ttu-id="2ded9-114">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ded9-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ded9-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="2ded9-115">-CipherSuite</span></span>
<span data-ttu-id="2ded9-116">Impostazioni delle suite crittografiche SSL nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="2ded9-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="2ded9-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ded9-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ded9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ded9-118">-DefaultProfile</span></span>
<span data-ttu-id="2ded9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ded9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ded9-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="2ded9-120">-FrontendProtocol</span></span>
<span data-ttu-id="2ded9-121">Impostazioni protocolli di sicurezza frontend.</span><span class="sxs-lookup"><span data-stu-id="2ded9-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="2ded9-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ded9-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ded9-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="2ded9-123">-ServerProtocol</span></span>
<span data-ttu-id="2ded9-124">Impostazioni del protocollo server come Http2.</span><span class="sxs-lookup"><span data-stu-id="2ded9-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="2ded9-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ded9-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ded9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ded9-126">CommonParameters</span></span>
<span data-ttu-id="2ded9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ded9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ded9-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ded9-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ded9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ded9-129">INPUTS</span></span>

### <span data-ttu-id="2ded9-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2ded9-130">None</span></span>

## <span data-ttu-id="2ded9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ded9-131">OUTPUTS</span></span>

### <span data-ttu-id="2ded9-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="2ded9-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="2ded9-133">Note</span><span class="sxs-lookup"><span data-stu-id="2ded9-133">NOTES</span></span>

## <span data-ttu-id="2ded9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ded9-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ded9-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ded9-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

