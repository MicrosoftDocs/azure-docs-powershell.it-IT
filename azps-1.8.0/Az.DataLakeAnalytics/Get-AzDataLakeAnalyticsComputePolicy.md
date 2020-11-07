---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684563"
---
# <span data-ttu-id="3c714-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c714-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c714-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c714-102">SYNOPSIS</span></span>
<span data-ttu-id="3c714-103">Ottiene un criterio di calcolo o un elenco di criteri di calcolo per i dati di Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c714-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="3c714-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c714-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c714-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c714-105">DESCRIPTION</span></span>
<span data-ttu-id="3c714-106">Il **Get-AzDataLakeAnalyticsComputePolicy** ottiene un criterio di calcolo di analisi dei dati di Azure Data Lake specificato o un elenco di criteri.</span><span class="sxs-lookup"><span data-stu-id="3c714-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="3c714-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c714-107">EXAMPLES</span></span>

### <span data-ttu-id="3c714-108">Esempio 1: ottenere un criterio di calcolo specificato</span><span class="sxs-lookup"><span data-stu-id="3c714-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="3c714-109">Questo comando ottiene il criterio di calcolo specificato con il nome "criterio" nell'account "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="3c714-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="3c714-110">Esempio 2: ottenere un elenco di tutti i criteri di calcolo nell'account</span><span class="sxs-lookup"><span data-stu-id="3c714-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="3c714-111">Questo comando consente di ottenere un elenco di tutti i criteri di calcolo nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="3c714-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="3c714-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c714-112">PARAMETERS</span></span>

### <span data-ttu-id="3c714-113">-Account</span><span class="sxs-lookup"><span data-stu-id="3c714-113">-Account</span></span>
<span data-ttu-id="3c714-114">Nome dell'account per ottenere i criteri di calcolo o i criteri.</span><span class="sxs-lookup"><span data-stu-id="3c714-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="3c714-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c714-115">-DefaultProfile</span></span>
<span data-ttu-id="3c714-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c714-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c714-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c714-117">-Name</span></span>
<span data-ttu-id="3c714-118">Nome del criterio di calcolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3c714-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="3c714-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c714-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c714-120">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="3c714-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3c714-121">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3c714-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3c714-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c714-122">CommonParameters</span></span>
<span data-ttu-id="3c714-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c714-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c714-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c714-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c714-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c714-125">INPUTS</span></span>

### <span data-ttu-id="3c714-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3c714-126">System.String</span></span>

## <span data-ttu-id="3c714-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c714-127">OUTPUTS</span></span>

### <span data-ttu-id="3c714-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c714-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c714-129">Note</span><span class="sxs-lookup"><span data-stu-id="3c714-129">NOTES</span></span>

## <span data-ttu-id="3c714-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c714-130">RELATED LINKS</span></span>