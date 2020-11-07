---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866746"
---
# <span data-ttu-id="8be1b-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="8be1b-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="8be1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8be1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8be1b-103">Crea un oggetto Configuration per le credenziali di SQL Server Key Vault in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be1b-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be1b-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8be1b-105">DESCRIPTION</span></span>

## <span data-ttu-id="8be1b-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be1b-106">EXAMPLES</span></span>

## <span data-ttu-id="8be1b-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8be1b-107">PARAMETERS</span></span>

### <span data-ttu-id="8be1b-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8be1b-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="8be1b-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8be1b-109">-CredentialName</span></span>
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

### <span data-ttu-id="8be1b-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="8be1b-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be1b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be1b-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be1b-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8be1b-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="8be1b-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="8be1b-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be1b-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8be1b-114">-Confirm</span></span>
<span data-ttu-id="8be1b-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be1b-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be1b-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be1b-116">-WhatIf</span></span>
<span data-ttu-id="8be1b-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be1b-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8be1b-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be1b-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be1b-119">CommonParameters</span></span>
<span data-ttu-id="8be1b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be1b-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be1b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be1b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8be1b-122">INPUTS</span></span>

### <span data-ttu-id="8be1b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8be1b-123">None</span></span>
<span data-ttu-id="8be1b-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8be1b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8be1b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be1b-125">OUTPUTS</span></span>

### <span data-ttu-id="8be1b-126">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8be1b-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="8be1b-127">Note</span><span class="sxs-lookup"><span data-stu-id="8be1b-127">NOTES</span></span>

## <span data-ttu-id="8be1b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be1b-128">RELATED LINKS</span></span>

