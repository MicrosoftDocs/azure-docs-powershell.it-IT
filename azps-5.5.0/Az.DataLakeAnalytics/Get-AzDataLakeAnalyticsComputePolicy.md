---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208666"
---
# <span data-ttu-id="226d3-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="226d3-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="226d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="226d3-102">SYNOPSIS</span></span>
<span data-ttu-id="226d3-103">Ottiene un criterio di calcolo Data Lake Analytics o un elenco di criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="226d3-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="226d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="226d3-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="226d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="226d3-105">DESCRIPTION</span></span>
<span data-ttu-id="226d3-106">Il **parametro Get-AzDataLakeAnalyticsComputePolicy** ottiene un criterio di calcolo Azure Data Lake Analytics specificato o un elenco di criteri.</span><span class="sxs-lookup"><span data-stu-id="226d3-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="226d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="226d3-107">EXAMPLES</span></span>

### <span data-ttu-id="226d3-108">Esempio 1: Ottenere un criterio di calcolo specificato</span><span class="sxs-lookup"><span data-stu-id="226d3-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="226d3-109">Questo comando recupera il criterio di calcolo specificato con il nome 'myPolicy' nell'account 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="226d3-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="226d3-110">Esempio 2: Ottenere un elenco di tutti i criteri di calcolo nell'account</span><span class="sxs-lookup"><span data-stu-id="226d3-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="226d3-111">Questo comando ottiene un elenco di tutti i criteri di calcolo nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="226d3-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="226d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="226d3-112">PARAMETERS</span></span>

### <span data-ttu-id="226d3-113">-Account</span><span class="sxs-lookup"><span data-stu-id="226d3-113">-Account</span></span>
<span data-ttu-id="226d3-114">Nome dell'account da cui recuperare i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="226d3-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226d3-115">-DefaultProfile</span></span>
<span data-ttu-id="226d3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="226d3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="226d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="226d3-117">-Name</span></span>
<span data-ttu-id="226d3-118">Nome del criterio di calcolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="226d3-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="226d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="226d3-120">Nome del gruppo di risorse in cui esiste l'account.</span><span class="sxs-lookup"><span data-stu-id="226d3-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="226d3-121">Facoltativo e tenterà di individuarne l'errore, se non specificato.</span><span class="sxs-lookup"><span data-stu-id="226d3-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="226d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226d3-122">CommonParameters</span></span>
<span data-ttu-id="226d3-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="226d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226d3-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226d3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226d3-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="226d3-125">INPUTS</span></span>

### <span data-ttu-id="226d3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="226d3-126">System.String</span></span>

## <span data-ttu-id="226d3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="226d3-127">OUTPUTS</span></span>

### <span data-ttu-id="226d3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="226d3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="226d3-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="226d3-129">NOTES</span></span>

## <span data-ttu-id="226d3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="226d3-130">RELATED LINKS</span></span>
