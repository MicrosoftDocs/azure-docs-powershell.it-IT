---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686842"
---
# <span data-ttu-id="d8845-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8845-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="d8845-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8845-102">SYNOPSIS</span></span>
<span data-ttu-id="d8845-103">Modifica la regola del firewall specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="d8845-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8845-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8845-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8845-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8845-105">DESCRIPTION</span></span>
<span data-ttu-id="d8845-106">Il cmdlet **set-AzureRmDataLakeStoreFirewallRule** modifica la regola del firewall specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d8845-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d8845-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8845-107">EXAMPLES</span></span>

### <span data-ttu-id="d8845-108">Esempio 1: aggiornare l'intervallo di inizio e di fine IP per una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="d8845-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="d8845-109">Aggiorna la regola del firewall "MyFirewallRule" nell'account "ContosoADL" per avere un intervallo di 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="d8845-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="d8845-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8845-110">PARAMETERS</span></span>

### <span data-ttu-id="d8845-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d8845-111">-Account</span></span>
<span data-ttu-id="d8845-112">L'account di data Lake Store per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="d8845-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="d8845-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d8845-113">-EndIpAddress</span></span>
<span data-ttu-id="d8845-114">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="d8845-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d8845-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8845-115">-Name</span></span>
<span data-ttu-id="d8845-116">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d8845-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d8845-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8845-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8845-118">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d8845-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="d8845-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d8845-119">-StartIpAddress</span></span>
<span data-ttu-id="d8845-120">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="d8845-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d8845-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8845-121">-Confirm</span></span>
<span data-ttu-id="d8845-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8845-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8845-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8845-123">-WhatIf</span></span>
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

### <span data-ttu-id="d8845-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8845-124">-DefaultProfile</span></span>
<span data-ttu-id="d8845-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8845-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8845-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8845-126">CommonParameters</span></span>
<span data-ttu-id="d8845-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8845-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8845-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8845-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8845-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8845-129">INPUTS</span></span>

## <span data-ttu-id="d8845-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8845-130">OUTPUTS</span></span>

### <span data-ttu-id="d8845-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8845-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="d8845-132">Dettagli della regola del firewall aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d8845-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="d8845-133">Note</span><span class="sxs-lookup"><span data-stu-id="d8845-133">NOTES</span></span>

## <span data-ttu-id="d8845-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8845-134">RELATED LINKS</span></span>

