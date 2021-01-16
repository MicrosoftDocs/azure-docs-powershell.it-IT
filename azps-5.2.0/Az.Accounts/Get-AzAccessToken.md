---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333172"
---
# <span data-ttu-id="14025-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="14025-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="14025-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14025-102">SYNOPSIS</span></span>
<span data-ttu-id="14025-103">Ottenere un token di accesso non elaborato.</span><span class="sxs-lookup"><span data-stu-id="14025-103">Get raw access token.</span></span> <span data-ttu-id="14025-104">Quando si usa-ResourceUrl, verificare che il valore corrisponda all'ambiente Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="14025-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="14025-105">È possibile fare riferimento al valore di `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="14025-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="14025-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14025-106">SYNTAX</span></span>

### <span data-ttu-id="14025-107">KnownResourceTypeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14025-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14025-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="14025-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14025-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14025-109">DESCRIPTION</span></span>
<span data-ttu-id="14025-110">Ottenere il token di accesso</span><span class="sxs-lookup"><span data-stu-id="14025-110">Get access token</span></span>

## <span data-ttu-id="14025-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14025-111">EXAMPLES</span></span>

### <span data-ttu-id="14025-112">Esempio 1 ottenere un token di accesso non elaborato per endpoint ARM</span><span class="sxs-lookup"><span data-stu-id="14025-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="14025-113">Ottenere il token di accesso dell'endpoint ResourceManager per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="14025-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="14025-114">Esempio 2 ottenere un token di accesso non elaborato per l'endpoint AAD Graph</span><span class="sxs-lookup"><span data-stu-id="14025-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="14025-115">Ottenere il token di accesso dell'endpoint di AAD Graph per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="14025-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="14025-116">Esempio 3 ottenere un token di accesso non elaborato per l'endpoint AAD Graph</span><span class="sxs-lookup"><span data-stu-id="14025-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="14025-117">Ottenere il token di accesso dell'endpoint di AAD Graph per l'account corrente</span><span class="sxs-lookup"><span data-stu-id="14025-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="14025-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14025-118">PARAMETERS</span></span>

### <span data-ttu-id="14025-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14025-119">-DefaultProfile</span></span>
<span data-ttu-id="14025-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14025-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14025-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="14025-121">-ResourceTypeName</span></span>
<span data-ttu-id="14025-122">Nome tipo facoltativo di resouce, valori supportati: AadGraph, AnalysisServices, ARM, Attestation, batch, datalake, Vault, OperationalInsights, ResourceManager, sinapsi.</span><span class="sxs-lookup"><span data-stu-id="14025-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="14025-123">Il valore predefinito è ARM se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="14025-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="14025-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="14025-124">-ResourceUrl</span></span>
<span data-ttu-id="14025-125">URL della risorsa per il quale si richiede il token, ad esempio ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="14025-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="14025-126">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="14025-126">-TenantId</span></span>
<span data-ttu-id="14025-127">ID tenant facoltativo. usare l'ID tenant del contesto predefinito, se non specificato.</span><span class="sxs-lookup"><span data-stu-id="14025-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="14025-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14025-128">CommonParameters</span></span>
<span data-ttu-id="14025-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14025-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14025-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14025-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14025-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14025-131">INPUTS</span></span>

### <span data-ttu-id="14025-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14025-132">None</span></span>

## <span data-ttu-id="14025-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14025-133">OUTPUTS</span></span>

### <span data-ttu-id="14025-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14025-134">System.String</span></span>

## <span data-ttu-id="14025-135">Note</span><span class="sxs-lookup"><span data-stu-id="14025-135">NOTES</span></span>

## <span data-ttu-id="14025-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14025-136">RELATED LINKS</span></span>
