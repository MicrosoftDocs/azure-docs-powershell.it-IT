---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518128"
---
# <span data-ttu-id="ddc6d-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ddc6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc6d-103">Modifica la regola del firewall specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddc6d-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc6d-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc6d-106">Il cmdlet **set-AzureRmDataLakeStoreFirewallRule** modifica la regola del firewall specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ddc6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddc6d-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc6d-108">Esempio 1: aggiornare l'intervallo di inizio e di fine IP per una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="ddc6d-109">Aggiorna la regola del firewall "MyFirewallRule" nell'account "ContosoADL" per avere un intervallo di 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="ddc6d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddc6d-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc6d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ddc6d-111">-Account</span></span>
<span data-ttu-id="ddc6d-112">L'account di data Lake Store per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="ddc6d-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="ddc6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-113">-DefaultProfile</span></span>
<span data-ttu-id="ddc6d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ddc6d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddc6d-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ddc6d-115">-EndIpAddress</span></span>
<span data-ttu-id="ddc6d-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc6d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddc6d-117">-Name</span></span>
<span data-ttu-id="ddc6d-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ddc6d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc6d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddc6d-120">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc6d-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ddc6d-121">-StartIpAddress</span></span>
<span data-ttu-id="ddc6d-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc6d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddc6d-123">-Confirm</span></span>
<span data-ttu-id="ddc6d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc6d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc6d-125">-WhatIf</span></span>
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

### <span data-ttu-id="ddc6d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc6d-126">CommonParameters</span></span>
<span data-ttu-id="ddc6d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc6d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc6d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc6d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddc6d-129">INPUTS</span></span>

### <span data-ttu-id="ddc6d-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ddc6d-130">None</span></span>
<span data-ttu-id="ddc6d-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ddc6d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddc6d-132">OUTPUTS</span></span>

### <span data-ttu-id="ddc6d-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="ddc6d-134">Dettagli della regola del firewall aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ddc6d-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="ddc6d-135">Note</span><span class="sxs-lookup"><span data-stu-id="ddc6d-135">NOTES</span></span>

## <span data-ttu-id="ddc6d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddc6d-136">RELATED LINKS</span></span>

