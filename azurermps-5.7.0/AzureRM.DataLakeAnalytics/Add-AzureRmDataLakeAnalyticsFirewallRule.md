---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: bed4ec4fd3afdf0218f68d9e2e4c61c739db48ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518136"
---
# <span data-ttu-id="de3f8-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de3f8-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="de3f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="de3f8-103">Aggiunge una regola del firewall a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="de3f8-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de3f8-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de3f8-105">DESCRIPTION</span></span>
<span data-ttu-id="de3f8-106">Il cmdlet **Add-AzureRmDataLakeAnalyticsFirewallRule** aggiunge una regola del firewall a un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="de3f8-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="de3f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de3f8-107">EXAMPLES</span></span>

### <span data-ttu-id="de3f8-108">Esempio 1: aggiungere una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="de3f8-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="de3f8-109">Questo comando aggiunge la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct" con l'intervallo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="de3f8-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="de3f8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de3f8-110">PARAMETERS</span></span>

### <span data-ttu-id="de3f8-111">-Account</span><span class="sxs-lookup"><span data-stu-id="de3f8-111">-Account</span></span>
<span data-ttu-id="de3f8-112">L'account di analisi del lago dati per aggiungere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="de3f8-112">The Data Lake Analytics account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3f8-113">-DefaultProfile</span></span>
<span data-ttu-id="de3f8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="de3f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="de3f8-115">-EndIpAddress</span></span>
<span data-ttu-id="de3f8-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="de3f8-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="de3f8-117">-Name</span></span>
<span data-ttu-id="de3f8-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="de3f8-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="de3f8-120">Nome del gruppo di risorse in cui si vuole recuperare l'account.</span><span class="sxs-lookup"><span data-stu-id="de3f8-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="de3f8-121">-StartIpAddress</span></span>
<span data-ttu-id="de3f8-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="de3f8-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de3f8-123">-Confirm</span></span>
<span data-ttu-id="de3f8-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3f8-125">-WhatIf</span></span>
<span data-ttu-id="de3f8-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de3f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de3f8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de3f8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3f8-128">CommonParameters</span></span>
<span data-ttu-id="de3f8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3f8-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3f8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de3f8-131">INPUTS</span></span>

### <span data-ttu-id="de3f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="de3f8-132">System.String</span></span>

## <span data-ttu-id="de3f8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de3f8-133">OUTPUTS</span></span>

### <span data-ttu-id="de3f8-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de3f8-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="de3f8-135">Note</span><span class="sxs-lookup"><span data-stu-id="de3f8-135">NOTES</span></span>

## <span data-ttu-id="de3f8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de3f8-136">RELATED LINKS</span></span>

