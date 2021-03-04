---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 2b4b225ca050e3efedb1de1371006a4ffdb87587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952670"
---
# <span data-ttu-id="c830e-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="c830e-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="c830e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c830e-102">SYNOPSIS</span></span>
<span data-ttu-id="c830e-103">Tenta di abilitare il Vault delle chiavi gestito dall'utente per la crittografia dell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c830e-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c830e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c830e-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c830e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c830e-105">DESCRIPTION</span></span>
<span data-ttu-id="c830e-106">Il cmdlet **Enable-AzDataLakeStoreKeyVault** tenta di abilitare un Vault delle chiavi gestito dall'utente per la crittografia dell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c830e-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c830e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c830e-107">EXAMPLES</span></span>

### <span data-ttu-id="c830e-108">Esempio 1: Abilitare il Vault delle chiavi per l'account ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="c830e-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="c830e-109">Questo comando tenta di abilitare il Vault delle chiavi gestito dall'utente per l'account Data Lake Store denominato ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="c830e-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="c830e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c830e-110">PARAMETERS</span></span>

### <span data-ttu-id="c830e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c830e-111">-Account</span></span>
<span data-ttu-id="c830e-112">Account Data Lake Store per abilitare il Vault delle chiavi gestito dall'utente per</span><span class="sxs-lookup"><span data-stu-id="c830e-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c830e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c830e-113">-DefaultProfile</span></span>
<span data-ttu-id="c830e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c830e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c830e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c830e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c830e-116">Nome del gruppo di risorse associato all'account.</span><span class="sxs-lookup"><span data-stu-id="c830e-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="c830e-117">Se non è specificato, verrà eseguito un tentativo di individuare.</span><span class="sxs-lookup"><span data-stu-id="c830e-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="c830e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c830e-118">-Confirm</span></span>
<span data-ttu-id="c830e-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c830e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c830e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c830e-120">-WhatIf</span></span>
<span data-ttu-id="c830e-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c830e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c830e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c830e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c830e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c830e-123">CommonParameters</span></span>
<span data-ttu-id="c830e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c830e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c830e-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c830e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c830e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="c830e-126">INPUTS</span></span>

### <span data-ttu-id="c830e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c830e-127">System.String</span></span>

## <span data-ttu-id="c830e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c830e-128">OUTPUTS</span></span>

### <span data-ttu-id="c830e-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="c830e-129">System.Void</span></span>

## <span data-ttu-id="c830e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c830e-130">NOTES</span></span>

## <span data-ttu-id="c830e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c830e-131">RELATED LINKS</span></span>

[<span data-ttu-id="c830e-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c830e-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c830e-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c830e-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

