---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186182"
---
# <span data-ttu-id="67f7f-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67f7f-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="67f7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="67f7f-103">Recupera una regola del firewall o un elenco di regole del firewall da un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="67f7f-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="67f7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67f7f-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f7f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="67f7f-106">Il cmdlet **Get-AzDataLakeAnalyticsFirewallRule** recupera una regola del firewall o un elenco di regole del firewall da un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="67f7f-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="67f7f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67f7f-107">EXAMPLES</span></span>

### <span data-ttu-id="67f7f-108">Esempio 1: Ottenere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="67f7f-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="67f7f-109">Questo comando recupera la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="67f7f-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="67f7f-110">Esempio 2: Elencare tutte le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="67f7f-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="67f7f-111">Questo comando recupera tutte le regole del firewall dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="67f7f-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="67f7f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f7f-112">PARAMETERS</span></span>

### <span data-ttu-id="67f7f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="67f7f-113">-Account</span></span>
<span data-ttu-id="67f7f-114">Account Data Lake Analytics da cui ottenere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="67f7f-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="67f7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f7f-115">-DefaultProfile</span></span>
<span data-ttu-id="67f7f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="67f7f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f7f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="67f7f-117">-Name</span></span>
<span data-ttu-id="67f7f-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="67f7f-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="67f7f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f7f-119">-ResourceGroupName</span></span>
<span data-ttu-id="67f7f-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="67f7f-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="67f7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f7f-121">CommonParameters</span></span>
<span data-ttu-id="67f7f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f7f-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f7f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f7f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="67f7f-124">INPUTS</span></span>

### <span data-ttu-id="67f7f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="67f7f-125">System.String</span></span>

## <span data-ttu-id="67f7f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67f7f-126">OUTPUTS</span></span>

### <span data-ttu-id="67f7f-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67f7f-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="67f7f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="67f7f-128">NOTES</span></span>

## <span data-ttu-id="67f7f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67f7f-129">RELATED LINKS</span></span>
