---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 8d69a3297f23fdc9e4095a695ee790ae2476a136
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674843"
---
# <span data-ttu-id="98c5f-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98c5f-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="98c5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="98c5f-103">Aggiorna una regola del firewall in un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="98c5f-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="98c5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98c5f-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c5f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="98c5f-106">Il cmdlet **set-AzDataLakeAnalyticsFirewallRule** aggiorna una regola del firewall in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="98c5f-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="98c5f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="98c5f-108">Esempio 1: aggiornare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="98c5f-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="98c5f-109">Questo comando Aggiorna la regola del firewall denominata "regola del firewall" in account "ContosoAdlAcct" per avere il nuovo intervallo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="98c5f-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="98c5f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="98c5f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="98c5f-111">-Account</span></span>
<span data-ttu-id="98c5f-112">L'account di analisi del lago dati per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="98c5f-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="98c5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c5f-113">-DefaultProfile</span></span>
<span data-ttu-id="98c5f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98c5f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c5f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="98c5f-115">-EndIpAddress</span></span>
<span data-ttu-id="98c5f-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="98c5f-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="98c5f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="98c5f-117">-Name</span></span>
<span data-ttu-id="98c5f-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="98c5f-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="98c5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="98c5f-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="98c5f-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="98c5f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="98c5f-121">-StartIpAddress</span></span>
<span data-ttu-id="98c5f-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="98c5f-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="98c5f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98c5f-123">-Confirm</span></span>
<span data-ttu-id="98c5f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c5f-125">-WhatIf</span></span>
<span data-ttu-id="98c5f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c5f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c5f-128">CommonParameters</span></span>
<span data-ttu-id="98c5f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c5f-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c5f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98c5f-131">INPUTS</span></span>

### <span data-ttu-id="98c5f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="98c5f-132">System.String</span></span>

## <span data-ttu-id="98c5f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98c5f-133">OUTPUTS</span></span>

### <span data-ttu-id="98c5f-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98c5f-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="98c5f-135">Note</span><span class="sxs-lookup"><span data-stu-id="98c5f-135">NOTES</span></span>

## <span data-ttu-id="98c5f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98c5f-136">RELATED LINKS</span></span>
