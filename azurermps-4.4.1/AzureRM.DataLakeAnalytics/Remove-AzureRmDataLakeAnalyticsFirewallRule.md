---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: cca9a398ad216de1bb28aac128fd9642b79d2dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510656"
---
# <span data-ttu-id="c70c6-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c70c6-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c70c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c70c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c70c6-103">Rimuove una regola del firewall da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="c70c6-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c70c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c70c6-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c70c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c70c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c70c6-106">Il cmdlet **Remove-AzureRmDataLakeAnalyticsFirewallRule** rimuove una regola del firewall da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="c70c6-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c70c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c70c6-107">EXAMPLES</span></span>

### <span data-ttu-id="c70c6-108">Esempio 1: rimuovere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="c70c6-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="c70c6-109">Questo comando rimuove la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="c70c6-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="c70c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c70c6-110">PARAMETERS</span></span>

### <span data-ttu-id="c70c6-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c70c6-111">-Account</span></span>
<span data-ttu-id="c70c6-112">L'account di analisi del lago dati per rimuovere la regola del firewall da</span><span class="sxs-lookup"><span data-stu-id="c70c6-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="c70c6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c70c6-113">-Name</span></span>
<span data-ttu-id="c70c6-114">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="c70c6-114">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="c70c6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c70c6-115">-PassThru</span></span>
<span data-ttu-id="c70c6-116">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="c70c6-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="c70c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c70c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c70c6-118">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="c70c6-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="c70c6-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c70c6-119">-Confirm</span></span>
<span data-ttu-id="c70c6-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c70c6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c70c6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c70c6-121">-WhatIf</span></span>
<span data-ttu-id="c70c6-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c70c6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c70c6-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c70c6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c70c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70c6-124">-DefaultProfile</span></span>
<span data-ttu-id="c70c6-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c70c6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70c6-126">CommonParameters</span></span>
<span data-ttu-id="c70c6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c70c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70c6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c70c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70c6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c70c6-129">INPUTS</span></span>

### <span data-ttu-id="c70c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c70c6-130">System.String</span></span>
<span data-ttu-id="c70c6-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c70c6-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c70c6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c70c6-132">OUTPUTS</span></span>

### <span data-ttu-id="c70c6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c70c6-133">System.Boolean</span></span>

## <span data-ttu-id="c70c6-134">Note</span><span class="sxs-lookup"><span data-stu-id="c70c6-134">NOTES</span></span>

## <span data-ttu-id="c70c6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c70c6-135">RELATED LINKS</span></span>

