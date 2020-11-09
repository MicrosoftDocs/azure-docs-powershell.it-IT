---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298098"
---
# <span data-ttu-id="1f55a-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1f55a-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="1f55a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f55a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f55a-103">Recupera una regola del firewall o un elenco di regole del firewall da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="1f55a-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f55a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f55a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f55a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f55a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f55a-106">Il cmdlet **Get-AzDataLakeAnalyticsFirewallRule** recupera una regola del firewall o un elenco di regole firewall da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1f55a-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f55a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f55a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f55a-108">Esempio 1: ottenere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="1f55a-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="1f55a-109">Questo comando ottiene la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="1f55a-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="1f55a-110">Esempio 2: elencare tutte le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="1f55a-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="1f55a-111">Questo comando ottiene tutte le regole del firewall dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="1f55a-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="1f55a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f55a-112">PARAMETERS</span></span>

### <span data-ttu-id="1f55a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="1f55a-113">-Account</span></span>
<span data-ttu-id="1f55a-114">L'account di analisi dei dati del lago per ottenere la regola del firewall da</span><span class="sxs-lookup"><span data-stu-id="1f55a-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="1f55a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f55a-115">-DefaultProfile</span></span>
<span data-ttu-id="1f55a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f55a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f55a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f55a-117">-Name</span></span>
<span data-ttu-id="1f55a-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="1f55a-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f55a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f55a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f55a-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="1f55a-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f55a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f55a-121">CommonParameters</span></span>
<span data-ttu-id="1f55a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f55a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f55a-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f55a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f55a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f55a-124">INPUTS</span></span>

### <span data-ttu-id="1f55a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1f55a-125">System.String</span></span>

## <span data-ttu-id="1f55a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f55a-126">OUTPUTS</span></span>

### <span data-ttu-id="1f55a-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1f55a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="1f55a-128">Note</span><span class="sxs-lookup"><span data-stu-id="1f55a-128">NOTES</span></span>

## <span data-ttu-id="1f55a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f55a-129">RELATED LINKS</span></span>
