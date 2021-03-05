---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 9fbb2064a7b7869af450ad267f73c6dc2e2b9a9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010637"
---
# <span data-ttu-id="4a871-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4a871-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="4a871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a871-102">SYNOPSIS</span></span>
<span data-ttu-id="4a871-103">Aggiorna una regola del firewall in un account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4a871-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4a871-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a871-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a871-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a871-105">DESCRIPTION</span></span>
<span data-ttu-id="4a871-106">Il cmdlet **Set-AzDataLakeAnalyticsFirewallRule** aggiorna una regola del firewall in un account di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4a871-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4a871-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a871-107">EXAMPLES</span></span>

### <span data-ttu-id="4a871-108">Esempio 1: Aggiornare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4a871-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="4a871-109">Questo comando aggiorna la regola del firewall denominata "regola del firewall" nell'account "ContosoAdlAcct" in modo che abbia il nuovo intervallo IP: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="4a871-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="4a871-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a871-110">PARAMETERS</span></span>

### <span data-ttu-id="4a871-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4a871-111">-Account</span></span>
<span data-ttu-id="4a871-112">Account Di Data Lake Analytics per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="4a871-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="4a871-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a871-113">-DefaultProfile</span></span>
<span data-ttu-id="4a871-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a871-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a871-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a871-115">-EndIpAddress</span></span>
<span data-ttu-id="4a871-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4a871-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="4a871-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4a871-117">-Name</span></span>
<span data-ttu-id="4a871-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="4a871-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="4a871-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a871-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a871-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="4a871-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="4a871-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a871-121">-StartIpAddress</span></span>
<span data-ttu-id="4a871-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4a871-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="4a871-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a871-123">-Confirm</span></span>
<span data-ttu-id="4a871-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a871-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a871-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a871-125">-WhatIf</span></span>
<span data-ttu-id="4a871-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a871-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a871-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a871-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a871-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a871-128">CommonParameters</span></span>
<span data-ttu-id="4a871-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a871-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a871-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a871-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a871-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a871-131">INPUTS</span></span>

### <span data-ttu-id="4a871-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4a871-132">System.String</span></span>

## <span data-ttu-id="4a871-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a871-133">OUTPUTS</span></span>

### <span data-ttu-id="4a871-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4a871-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="4a871-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a871-135">NOTES</span></span>

## <span data-ttu-id="4a871-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a871-136">RELATED LINKS</span></span>
