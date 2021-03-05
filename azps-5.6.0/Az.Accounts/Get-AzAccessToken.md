---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973022"
---
# <span data-ttu-id="5d769-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="5d769-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="5d769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d769-102">SYNOPSIS</span></span>
<span data-ttu-id="5d769-103">Ottieni il token di accesso non elaborato.</span><span class="sxs-lookup"><span data-stu-id="5d769-103">Get raw access token.</span></span> <span data-ttu-id="5d769-104">Quando si usa -ResourceUrl, verificare che il valore corrisponda all'ambiente Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5d769-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="5d769-105">È possibile fare riferimento al valore di `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="5d769-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="5d769-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d769-106">SYNTAX</span></span>

### <span data-ttu-id="5d769-107">KnownResourceTypeName (Default)</span><span class="sxs-lookup"><span data-stu-id="5d769-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d769-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="5d769-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d769-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d769-109">DESCRIPTION</span></span>
<span data-ttu-id="5d769-110">Ottieni token di accesso</span><span class="sxs-lookup"><span data-stu-id="5d769-110">Get access token</span></span>

## <span data-ttu-id="5d769-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d769-111">EXAMPLES</span></span>

### <span data-ttu-id="5d769-112">Esempio 1 Ottenere il token di accesso non elaborati per ARM endpoint</span><span class="sxs-lookup"><span data-stu-id="5d769-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="5d769-113">Ottenere il token di accesso dell'endpoint ResourceManager per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="5d769-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="5d769-114">Esempio 2: Ottenere il token di accesso non elaborato per l'endpoint del grafico AAD</span><span class="sxs-lookup"><span data-stu-id="5d769-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="5d769-115">Ottenere il token di accesso dell'endpoint grafico AAD per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="5d769-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="5d769-116">Esempio 3: Ottenere il token di accesso non elaborato per l'endpoint del grafico AAD</span><span class="sxs-lookup"><span data-stu-id="5d769-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="5d769-117">Ottenere il token di accesso dell'endpoint grafico AAD per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="5d769-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="5d769-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d769-118">PARAMETERS</span></span>

### <span data-ttu-id="5d769-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d769-119">-DefaultProfile</span></span>
<span data-ttu-id="5d769-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d769-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d769-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="5d769-121">-ResourceTypeName</span></span>
<span data-ttu-id="5d769-122">Nome del tipo di resouce facoltativo, valori supportati: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d769-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="5d769-123">Il valore predefinito è Arm, se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="5d769-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d769-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="5d769-124">-ResourceUrl</span></span>
<span data-ttu-id="5d769-125">URL della risorsa per il token richiesto, ad esempio ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="5d769-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d769-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5d769-126">-TenantId</span></span>
<span data-ttu-id="5d769-127">ID tenant facoltativo. Se non viene specificato, usare l'ID tenant del contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="5d769-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="5d769-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d769-128">CommonParameters</span></span>
<span data-ttu-id="5d769-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d769-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d769-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d769-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d769-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d769-131">INPUTS</span></span>

### <span data-ttu-id="5d769-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5d769-132">None</span></span>

## <span data-ttu-id="5d769-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d769-133">OUTPUTS</span></span>

### <span data-ttu-id="5d769-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5d769-134">System.String</span></span>

## <span data-ttu-id="5d769-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d769-135">NOTES</span></span>

## <span data-ttu-id="5d769-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d769-136">RELATED LINKS</span></span>
