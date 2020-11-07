---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6d179a4cc5814c45925802f606480927a3ed3af0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684547"
---
# <span data-ttu-id="0c824-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0c824-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0c824-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c824-102">SYNOPSIS</span></span>
<span data-ttu-id="0c824-103">Rimuove una regola del firewall da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="0c824-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0c824-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c824-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c824-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c824-105">DESCRIPTION</span></span>
<span data-ttu-id="0c824-106">Il cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** rimuove una regola del firewall da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0c824-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0c824-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c824-107">EXAMPLES</span></span>

### <span data-ttu-id="0c824-108">Esempio 1: rimuovere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="0c824-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0c824-109">Questo comando rimuove la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="0c824-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0c824-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c824-110">PARAMETERS</span></span>

### <span data-ttu-id="0c824-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0c824-111">-Account</span></span>
<span data-ttu-id="0c824-112">L'account di analisi del lago dati per rimuovere la regola del firewall da</span><span class="sxs-lookup"><span data-stu-id="0c824-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="0c824-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c824-113">-DefaultProfile</span></span>
<span data-ttu-id="0c824-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c824-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c824-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c824-115">-Name</span></span>
<span data-ttu-id="0c824-116">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="0c824-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0c824-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c824-117">-PassThru</span></span>
<span data-ttu-id="0c824-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="0c824-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0c824-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c824-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c824-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="0c824-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="0c824-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c824-121">-Confirm</span></span>
<span data-ttu-id="0c824-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c824-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c824-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c824-123">-WhatIf</span></span>
<span data-ttu-id="0c824-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c824-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c824-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c824-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c824-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c824-126">CommonParameters</span></span>
<span data-ttu-id="0c824-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c824-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c824-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c824-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c824-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c824-129">INPUTS</span></span>

### <span data-ttu-id="0c824-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0c824-130">System.String</span></span>

### <span data-ttu-id="0c824-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c824-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c824-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c824-132">OUTPUTS</span></span>

### <span data-ttu-id="0c824-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c824-133">System.Boolean</span></span>

## <span data-ttu-id="0c824-134">Note</span><span class="sxs-lookup"><span data-stu-id="0c824-134">NOTES</span></span>

## <span data-ttu-id="0c824-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c824-135">RELATED LINKS</span></span>
