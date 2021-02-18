---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181566"
---
# <span data-ttu-id="3e7e4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="3e7e4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="3e7e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e7e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7e4-103">Crea un oggetto di configurazione per SQL credenziali del vault con chiave del server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="3e7e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e7e4-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e7e4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e7e4-105">DESCRIPTION</span></span>

## <span data-ttu-id="3e7e4-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e7e4-106">EXAMPLES</span></span>

## <span data-ttu-id="3e7e4-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e7e4-107">PARAMETERS</span></span>

### <span data-ttu-id="3e7e4-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="3e7e4-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="3e7e4-109">URL del servizio Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="3e7e4-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="3e7e4-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="3e7e4-110">-CredentialName</span></span>
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

### <span data-ttu-id="3e7e4-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="3e7e4-111">-Enable</span></span>
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

### <span data-ttu-id="3e7e4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e7e4-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3e7e4-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3e7e4-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="3e7e4-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="3e7e4-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="3e7e4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e7e4-115">-Confirm</span></span>
<span data-ttu-id="3e7e4-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e7e4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e7e4-117">-WhatIf</span></span>
<span data-ttu-id="3e7e4-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e7e4-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e7e4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7e4-120">CommonParameters</span></span>
<span data-ttu-id="3e7e4-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7e4-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7e4-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e7e4-123">INPUTS</span></span>

### <span data-ttu-id="3e7e4-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3e7e4-124">System.String</span></span>

### <span data-ttu-id="3e7e4-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e7e4-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3e7e4-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="3e7e4-126">System.Security.SecureString</span></span>

## <span data-ttu-id="3e7e4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e7e4-127">OUTPUTS</span></span>

### <span data-ttu-id="3e7e4-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="3e7e4-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="3e7e4-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e7e4-129">NOTES</span></span>

## <span data-ttu-id="3e7e4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e7e4-130">RELATED LINKS</span></span>
