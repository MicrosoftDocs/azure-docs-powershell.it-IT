---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94023001"
---
# <span data-ttu-id="2d5fe-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d5fe-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2d5fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2d5fe-103">Aggiunge una regola del firewall a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2d5fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d5fe-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d5fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="2d5fe-106">Il cmdlet **Add-AzDataLakeAnalyticsFirewallRule** aggiunge una regola del firewall a un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2d5fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d5fe-107">EXAMPLES</span></span>

### <span data-ttu-id="2d5fe-108">Esempio 1: aggiungere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="2d5fe-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="2d5fe-109">Questo comando aggiunge la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct" con l'intervallo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="2d5fe-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="2d5fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d5fe-110">PARAMETERS</span></span>

### <span data-ttu-id="2d5fe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="2d5fe-111">-Account</span></span>
<span data-ttu-id="2d5fe-112">L'account di analisi del lago dati per aggiungere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="2d5fe-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="2d5fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d5fe-113">-DefaultProfile</span></span>
<span data-ttu-id="2d5fe-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2d5fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d5fe-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2d5fe-115">-EndIpAddress</span></span>
<span data-ttu-id="2d5fe-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="2d5fe-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="2d5fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d5fe-117">-Name</span></span>
<span data-ttu-id="2d5fe-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="2d5fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d5fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d5fe-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="2d5fe-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2d5fe-121">-StartIpAddress</span></span>
<span data-ttu-id="2d5fe-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="2d5fe-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="2d5fe-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d5fe-123">-Confirm</span></span>
<span data-ttu-id="2d5fe-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d5fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d5fe-125">-WhatIf</span></span>
<span data-ttu-id="2d5fe-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d5fe-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d5fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d5fe-128">CommonParameters</span></span>
<span data-ttu-id="2d5fe-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d5fe-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d5fe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d5fe-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d5fe-131">INPUTS</span></span>

### <span data-ttu-id="2d5fe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d5fe-132">System.String</span></span>

## <span data-ttu-id="2d5fe-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d5fe-133">OUTPUTS</span></span>

### <span data-ttu-id="2d5fe-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d5fe-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2d5fe-135">Note</span><span class="sxs-lookup"><span data-stu-id="2d5fe-135">NOTES</span></span>

## <span data-ttu-id="2d5fe-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d5fe-136">RELATED LINKS</span></span>
