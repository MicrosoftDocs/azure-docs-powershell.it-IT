---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863614"
---
# <span data-ttu-id="e6189-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="e6189-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="e6189-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6189-102">SYNOPSIS</span></span>
<span data-ttu-id="e6189-103">Crea un oggetto Configuration per le credenziali di SQL Server Key Vault in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6189-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="e6189-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6189-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6189-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6189-105">DESCRIPTION</span></span>

## <span data-ttu-id="e6189-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6189-106">EXAMPLES</span></span>

## <span data-ttu-id="e6189-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6189-107">PARAMETERS</span></span>

### <span data-ttu-id="e6189-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e6189-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="e6189-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e6189-109">-CredentialName</span></span>
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

### <span data-ttu-id="e6189-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="e6189-110">-Enable</span></span>
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

### <span data-ttu-id="e6189-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6189-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e6189-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e6189-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="e6189-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="e6189-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="e6189-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6189-114">-Confirm</span></span>
<span data-ttu-id="e6189-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6189-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6189-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6189-116">-WhatIf</span></span>
<span data-ttu-id="e6189-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6189-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e6189-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6189-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6189-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6189-119">CommonParameters</span></span>
<span data-ttu-id="e6189-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6189-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6189-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6189-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6189-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6189-122">INPUTS</span></span>

### <span data-ttu-id="e6189-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6189-123">None</span></span>
<span data-ttu-id="e6189-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6189-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6189-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6189-125">OUTPUTS</span></span>

### <span data-ttu-id="e6189-126">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e6189-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="e6189-127">Note</span><span class="sxs-lookup"><span data-stu-id="e6189-127">NOTES</span></span>

## <span data-ttu-id="e6189-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6189-128">RELATED LINKS</span></span>

