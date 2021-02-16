---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201478"
---
# <span data-ttu-id="0b307-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0b307-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="0b307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b307-102">SYNOPSIS</span></span>
<span data-ttu-id="0b307-103">Ottiene la protezione TDE (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="0b307-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="0b307-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b307-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b307-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b307-105">DESCRIPTION</span></span>
<span data-ttu-id="0b307-106">Il Get-AzSqlServerTransparentDataEncryptionProtector cmdlet riceve informazioni sulla protezione TDE.</span><span class="sxs-lookup"><span data-stu-id="0b307-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="0b307-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b307-107">EXAMPLES</span></span>

### <span data-ttu-id="0b307-108">Esempio 1: Ottenere la protezione TDE (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="0b307-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="0b307-109">Questo comando ottiene la protezione TDE per il server denominato ContosoServer nel gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b307-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="0b307-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="0b307-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="0b307-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="0b307-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="0b307-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b307-112">PARAMETERS</span></span>

### <span data-ttu-id="0b307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b307-113">-DefaultProfile</span></span>
<span data-ttu-id="0b307-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0b307-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b307-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b307-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b307-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0b307-116">The name of the resource group</span></span>

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

### <span data-ttu-id="0b307-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b307-117">-ServerName</span></span>
<span data-ttu-id="0b307-118">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b307-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0b307-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b307-119">-Confirm</span></span>
<span data-ttu-id="0b307-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b307-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b307-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b307-121">-WhatIf</span></span>
<span data-ttu-id="0b307-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b307-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b307-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b307-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b307-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b307-124">CommonParameters</span></span>
<span data-ttu-id="0b307-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b307-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b307-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b307-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b307-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b307-127">INPUTS</span></span>

### <span data-ttu-id="0b307-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0b307-128">System.String</span></span>

## <span data-ttu-id="0b307-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b307-129">OUTPUTS</span></span>

### <span data-ttu-id="0b307-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="0b307-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="0b307-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b307-131">NOTES</span></span>

## <span data-ttu-id="0b307-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b307-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b307-133">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="0b307-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
