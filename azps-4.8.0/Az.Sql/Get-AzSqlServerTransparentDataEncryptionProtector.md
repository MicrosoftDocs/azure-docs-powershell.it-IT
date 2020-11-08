---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190078"
---
# <span data-ttu-id="ab2a5-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ab2a5-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="ab2a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2a5-103">Ottiene la protezione da crittografia dati trasparente (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="ab2a5-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="ab2a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab2a5-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab2a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2a5-106">Il cmdlet Get-AzSqlServerTransparentDataEncryptionProtector ottiene le informazioni relative al Protector di Transportation.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="ab2a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab2a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2a5-108">Esempio 1: ottenere la protezione da crittografia dati trasparente (Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="ab2a5-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="ab2a5-109">Questo comando consente di ottenere la protezione di Transparent per il server denominato ContosoServer nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ab2a5-110">ResourceGroupName nomeserver tipo ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="ab2a5-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="ab2a5-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="ab2a5-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="ab2a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab2a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ab2a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2a5-113">-DefaultProfile</span></span>
<span data-ttu-id="ab2a5-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab2a5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab2a5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2a5-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab2a5-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ab2a5-116">The name of the resource group</span></span>

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

### <span data-ttu-id="ab2a5-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ab2a5-117">-ServerName</span></span>
<span data-ttu-id="ab2a5-118">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ab2a5-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab2a5-119">-Confirm</span></span>
<span data-ttu-id="ab2a5-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2a5-121">-WhatIf</span></span>
<span data-ttu-id="ab2a5-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2a5-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2a5-124">CommonParameters</span></span>
<span data-ttu-id="ab2a5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2a5-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2a5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab2a5-127">INPUTS</span></span>

### <span data-ttu-id="ab2a5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ab2a5-128">System.String</span></span>

## <span data-ttu-id="ab2a5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab2a5-129">OUTPUTS</span></span>

### <span data-ttu-id="ab2a5-130">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="ab2a5-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="ab2a5-131">Note</span><span class="sxs-lookup"><span data-stu-id="ab2a5-131">NOTES</span></span>

## <span data-ttu-id="ab2a5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab2a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab2a5-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ab2a5-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)