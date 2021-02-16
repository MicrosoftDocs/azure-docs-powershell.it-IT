---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194742"
---
# <span data-ttu-id="e13be-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e13be-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e13be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e13be-102">SYNOPSIS</span></span>
<span data-ttu-id="e13be-103">Aggiorna una regola del firewall in un account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e13be-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e13be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e13be-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e13be-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e13be-105">DESCRIPTION</span></span>
<span data-ttu-id="e13be-106">Il cmdlet **Set-AzDataLakeAnalyticsFirewallRule** aggiorna una regola del firewall in un account di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e13be-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e13be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e13be-107">EXAMPLES</span></span>

### <span data-ttu-id="e13be-108">Esempio 1: Aggiornare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e13be-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="e13be-109">Questo comando aggiorna la regola del firewall denominata "regola del firewall" nell'account "ContosoAdlAcct" in modo che abbia il nuovo intervallo IP: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="e13be-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="e13be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e13be-110">PARAMETERS</span></span>

### <span data-ttu-id="e13be-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e13be-111">-Account</span></span>
<span data-ttu-id="e13be-112">Account di Data Lake Analytics per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="e13be-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="e13be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13be-113">-DefaultProfile</span></span>
<span data-ttu-id="e13be-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e13be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e13be-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e13be-115">-EndIpAddress</span></span>
<span data-ttu-id="e13be-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e13be-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13be-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e13be-117">-Name</span></span>
<span data-ttu-id="e13be-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e13be-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e13be-119">-ResourceGroupName</span></span>
<span data-ttu-id="e13be-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="e13be-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="e13be-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e13be-121">-StartIpAddress</span></span>
<span data-ttu-id="e13be-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e13be-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="e13be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e13be-123">-Confirm</span></span>
<span data-ttu-id="e13be-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e13be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13be-125">-WhatIf</span></span>
<span data-ttu-id="e13be-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e13be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e13be-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e13be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e13be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13be-128">CommonParameters</span></span>
<span data-ttu-id="e13be-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13be-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13be-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e13be-131">INPUTS</span></span>

### <span data-ttu-id="e13be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e13be-132">System.String</span></span>

## <span data-ttu-id="e13be-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e13be-133">OUTPUTS</span></span>

### <span data-ttu-id="e13be-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e13be-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e13be-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e13be-135">NOTES</span></span>

## <span data-ttu-id="e13be-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e13be-136">RELATED LINKS</span></span>
