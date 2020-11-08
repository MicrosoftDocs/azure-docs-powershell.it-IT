---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031303"
---
# <span data-ttu-id="40949-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="40949-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="40949-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40949-102">SYNOPSIS</span></span>
<span data-ttu-id="40949-103">Modifica la regola del firewall specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="40949-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="40949-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40949-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40949-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40949-105">DESCRIPTION</span></span>
<span data-ttu-id="40949-106">Il cmdlet **set-AzDataLakeStoreFirewallRule** modifica la regola del firewall specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="40949-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="40949-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40949-107">EXAMPLES</span></span>

### <span data-ttu-id="40949-108">Esempio 1: aggiornare l'intervallo di inizio e di fine IP per una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="40949-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="40949-109">Aggiorna la regola del firewall "MyFirewallRule" nell'account "ContosoADL" per avere un intervallo di 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="40949-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="40949-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40949-110">PARAMETERS</span></span>

### <span data-ttu-id="40949-111">-Account</span><span class="sxs-lookup"><span data-stu-id="40949-111">-Account</span></span>
<span data-ttu-id="40949-112">L'account di data Lake Store per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="40949-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="40949-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40949-113">-DefaultProfile</span></span>
<span data-ttu-id="40949-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="40949-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40949-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="40949-115">-EndIpAddress</span></span>
<span data-ttu-id="40949-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="40949-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="40949-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="40949-117">-Name</span></span>
<span data-ttu-id="40949-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="40949-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="40949-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40949-119">-ResourceGroupName</span></span>
<span data-ttu-id="40949-120">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="40949-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="40949-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="40949-121">-StartIpAddress</span></span>
<span data-ttu-id="40949-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="40949-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="40949-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40949-123">-Confirm</span></span>
<span data-ttu-id="40949-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40949-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40949-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40949-125">-WhatIf</span></span>
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

### <span data-ttu-id="40949-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40949-126">CommonParameters</span></span>
<span data-ttu-id="40949-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40949-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40949-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40949-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40949-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40949-129">INPUTS</span></span>

### <span data-ttu-id="40949-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40949-130">System.String</span></span>

## <span data-ttu-id="40949-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40949-131">OUTPUTS</span></span>

### <span data-ttu-id="40949-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="40949-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="40949-133">Note</span><span class="sxs-lookup"><span data-stu-id="40949-133">NOTES</span></span>

## <span data-ttu-id="40949-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40949-134">RELATED LINKS</span></span>
