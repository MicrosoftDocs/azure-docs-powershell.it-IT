---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864548"
---
# <span data-ttu-id="c3ce4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="c3ce4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="c3ce4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ce4-103">Crea un oggetto Configuration per le credenziali di SQL Server Key Vault in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3ce4-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="c3ce4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3ce4-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ce4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3ce4-105">DESCRIPTION</span></span>

## <span data-ttu-id="c3ce4-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3ce4-106">EXAMPLES</span></span>

## <span data-ttu-id="c3ce4-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3ce4-107">PARAMETERS</span></span>

### <span data-ttu-id="c3ce4-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="c3ce4-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="c3ce4-109">URL del servizio di archiviazione delle chiavi di Azure</span><span class="sxs-lookup"><span data-stu-id="c3ce4-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="c3ce4-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="c3ce4-110">-CredentialName</span></span>
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

### <span data-ttu-id="c3ce4-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="c3ce4-111">-Enable</span></span>
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

### <span data-ttu-id="c3ce4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ce4-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c3ce4-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c3ce4-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="c3ce4-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="c3ce4-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="c3ce4-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3ce4-115">-Confirm</span></span>
<span data-ttu-id="c3ce4-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3ce4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ce4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ce4-117">-WhatIf</span></span>
<span data-ttu-id="c3ce4-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3ce4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ce4-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3ce4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ce4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ce4-120">CommonParameters</span></span>
<span data-ttu-id="c3ce4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ce4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ce4-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3ce4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ce4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3ce4-123">INPUTS</span></span>

### <span data-ttu-id="c3ce4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c3ce4-124">System.String</span></span>

### <span data-ttu-id="c3ce4-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3ce4-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c3ce4-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c3ce4-126">System.Security.SecureString</span></span>

## <span data-ttu-id="c3ce4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3ce4-127">OUTPUTS</span></span>

### <span data-ttu-id="c3ce4-128">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="c3ce4-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="c3ce4-129">Note</span><span class="sxs-lookup"><span data-stu-id="c3ce4-129">NOTES</span></span>

## <span data-ttu-id="c3ce4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3ce4-130">RELATED LINKS</span></span>
