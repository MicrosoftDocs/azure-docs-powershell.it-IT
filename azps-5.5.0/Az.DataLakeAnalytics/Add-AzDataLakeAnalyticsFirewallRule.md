---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208675"
---
# <span data-ttu-id="51f6e-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51f6e-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="51f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="51f6e-103">Aggiunge una regola del firewall a un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51f6e-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="51f6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51f6e-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f6e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="51f6e-106">Il cmdlet **Add-AzDataLakeAnalyticsFirewallRule** aggiunge una regola del firewall a un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51f6e-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="51f6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51f6e-107">EXAMPLES</span></span>

### <span data-ttu-id="51f6e-108">Esempio 1: Aggiungere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="51f6e-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="51f6e-109">Questo comando aggiunge la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct" con l'intervallo IP: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="51f6e-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="51f6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51f6e-110">PARAMETERS</span></span>

### <span data-ttu-id="51f6e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="51f6e-111">-Account</span></span>
<span data-ttu-id="51f6e-112">Account di Data Lake Analytics a cui aggiungere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="51f6e-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="51f6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f6e-113">-DefaultProfile</span></span>
<span data-ttu-id="51f6e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="51f6e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51f6e-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="51f6e-115">-EndIpAddress</span></span>
<span data-ttu-id="51f6e-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="51f6e-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f6e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="51f6e-117">-Name</span></span>
<span data-ttu-id="51f6e-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="51f6e-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="51f6e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f6e-119">-ResourceGroupName</span></span>
<span data-ttu-id="51f6e-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="51f6e-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="51f6e-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="51f6e-121">-StartIpAddress</span></span>
<span data-ttu-id="51f6e-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="51f6e-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f6e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51f6e-123">-Confirm</span></span>
<span data-ttu-id="51f6e-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f6e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f6e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f6e-125">-WhatIf</span></span>
<span data-ttu-id="51f6e-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51f6e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f6e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51f6e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f6e-128">CommonParameters</span></span>
<span data-ttu-id="51f6e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f6e-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f6e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f6e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="51f6e-131">INPUTS</span></span>

### <span data-ttu-id="51f6e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="51f6e-132">System.String</span></span>

## <span data-ttu-id="51f6e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51f6e-133">OUTPUTS</span></span>

### <span data-ttu-id="51f6e-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51f6e-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="51f6e-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="51f6e-135">NOTES</span></span>

## <span data-ttu-id="51f6e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51f6e-136">RELATED LINKS</span></span>
