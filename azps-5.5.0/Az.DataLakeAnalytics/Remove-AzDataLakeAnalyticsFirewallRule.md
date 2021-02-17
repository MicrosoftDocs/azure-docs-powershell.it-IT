---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194790"
---
# <span data-ttu-id="6e9fe-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e9fe-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6e9fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9fe-103">Rimuove una regola del firewall da un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6e9fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e9fe-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e9fe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e9fe-105">DESCRIPTION</span></span>
<span data-ttu-id="6e9fe-106">Il cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** rimuove una regola del firewall da un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6e9fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e9fe-107">EXAMPLES</span></span>

### <span data-ttu-id="6e9fe-108">Esempio 1: Rimuovere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="6e9fe-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="6e9fe-109">Questo comando rimuove la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="6e9fe-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="6e9fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e9fe-110">PARAMETERS</span></span>

### <span data-ttu-id="6e9fe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6e9fe-111">-Account</span></span>
<span data-ttu-id="6e9fe-112">Account di Data Lake Analytics da cui rimuovere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="6e9fe-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="6e9fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9fe-113">-DefaultProfile</span></span>
<span data-ttu-id="6e9fe-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6e9fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e9fe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e9fe-115">-Name</span></span>
<span data-ttu-id="6e9fe-116">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="6e9fe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e9fe-117">-PassThru</span></span>
<span data-ttu-id="6e9fe-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e9fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e9fe-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="6e9fe-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e9fe-121">-Confirm</span></span>
<span data-ttu-id="6e9fe-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9fe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e9fe-123">-WhatIf</span></span>
<span data-ttu-id="6e9fe-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e9fe-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9fe-126">CommonParameters</span></span>
<span data-ttu-id="6e9fe-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9fe-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9fe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9fe-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e9fe-129">INPUTS</span></span>

### <span data-ttu-id="6e9fe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6e9fe-130">System.String</span></span>

### <span data-ttu-id="6e9fe-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e9fe-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e9fe-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e9fe-132">OUTPUTS</span></span>

### <span data-ttu-id="6e9fe-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e9fe-133">System.Boolean</span></span>

## <span data-ttu-id="6e9fe-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e9fe-134">NOTES</span></span>

## <span data-ttu-id="6e9fe-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e9fe-135">RELATED LINKS</span></span>
