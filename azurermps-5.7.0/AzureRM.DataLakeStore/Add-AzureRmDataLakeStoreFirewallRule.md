---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521053"
---
# <span data-ttu-id="15525-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="15525-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="15525-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15525-102">SYNOPSIS</span></span>
<span data-ttu-id="15525-103">Aggiunge una regola del firewall all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="15525-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15525-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15525-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15525-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15525-105">DESCRIPTION</span></span>
<span data-ttu-id="15525-106">Il cmdlet **Add-AzureRmDataLakeStoreFirewallRule** aggiunge una regola del firewall all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="15525-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="15525-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15525-107">EXAMPLES</span></span>

### <span data-ttu-id="15525-108">Esempio 1: aggiungere una nuova regola del firewall a un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="15525-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="15525-109">In questo modo viene creata una nuova regola del firewall denominata "regola" in account "ContosoADL" con un intervallo IP di 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="15525-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="15525-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15525-110">PARAMETERS</span></span>

### <span data-ttu-id="15525-111">-Account</span><span class="sxs-lookup"><span data-stu-id="15525-111">-Account</span></span>
<span data-ttu-id="15525-112">L'account di data Lake Store per aggiungere la regola del firewall a</span><span class="sxs-lookup"><span data-stu-id="15525-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="15525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15525-113">-DefaultProfile</span></span>
<span data-ttu-id="15525-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="15525-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15525-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="15525-115">-EndIpAddress</span></span>
<span data-ttu-id="15525-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="15525-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="15525-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="15525-117">-Name</span></span>
<span data-ttu-id="15525-118">Nome della regola del firewall da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="15525-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="15525-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15525-119">-ResourceGroupName</span></span>
<span data-ttu-id="15525-120">Nome del gruppo di risorse in cui si trova l'account per aggiungere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="15525-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15525-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="15525-121">-StartIpAddress</span></span>
<span data-ttu-id="15525-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="15525-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="15525-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15525-123">-Confirm</span></span>
<span data-ttu-id="15525-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15525-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15525-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15525-125">-WhatIf</span></span>
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

### <span data-ttu-id="15525-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15525-126">CommonParameters</span></span>
<span data-ttu-id="15525-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15525-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15525-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15525-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15525-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15525-129">INPUTS</span></span>

### <span data-ttu-id="15525-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="15525-130">None</span></span>
<span data-ttu-id="15525-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="15525-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15525-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15525-132">OUTPUTS</span></span>

### <span data-ttu-id="15525-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="15525-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="15525-134">Regola del firewall aggiunta.</span><span class="sxs-lookup"><span data-stu-id="15525-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="15525-135">Note</span><span class="sxs-lookup"><span data-stu-id="15525-135">NOTES</span></span>

## <span data-ttu-id="15525-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15525-136">RELATED LINKS</span></span>

