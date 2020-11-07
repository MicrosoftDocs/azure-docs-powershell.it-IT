---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686457"
---
# <span data-ttu-id="867af-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="867af-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="867af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="867af-102">SYNOPSIS</span></span>
<span data-ttu-id="867af-103">Crea un oggetto Configuration per le credenziali di SQL Server Key Vault in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="867af-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="867af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="867af-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="867af-105">DESCRIPTION</span></span>

## <span data-ttu-id="867af-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="867af-106">EXAMPLES</span></span>

## <span data-ttu-id="867af-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="867af-107">PARAMETERS</span></span>

### <span data-ttu-id="867af-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="867af-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="867af-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="867af-109">-CredentialName</span></span>
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

### <span data-ttu-id="867af-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="867af-110">-Enable</span></span>
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

### <span data-ttu-id="867af-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867af-111">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867af-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="867af-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="867af-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="867af-113">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867af-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="867af-114">-Confirm</span></span>
<span data-ttu-id="867af-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="867af-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867af-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867af-116">-WhatIf</span></span>
<span data-ttu-id="867af-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="867af-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867af-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="867af-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867af-119">CommonParameters</span></span>
<span data-ttu-id="867af-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867af-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867af-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="867af-122">INPUTS</span></span>

### <span data-ttu-id="867af-123">System. String</span><span class="sxs-lookup"><span data-stu-id="867af-123">System.String</span></span>

### <span data-ttu-id="867af-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="867af-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="867af-125">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="867af-125">System.Security.SecureString</span></span>

## <span data-ttu-id="867af-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="867af-126">OUTPUTS</span></span>

### <span data-ttu-id="867af-127">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="867af-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="867af-128">Note</span><span class="sxs-lookup"><span data-stu-id="867af-128">NOTES</span></span>

## <span data-ttu-id="867af-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="867af-129">RELATED LINKS</span></span>
