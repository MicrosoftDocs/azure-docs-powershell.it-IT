---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 0e8adfc9ef5cfd5525a0e07b35c3eb1b918b9ba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684540"
---
# <span data-ttu-id="a177d-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="a177d-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="a177d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a177d-102">SYNOPSIS</span></span>
<span data-ttu-id="a177d-103">Consente di consentire a un Vault Key gestito dall'utente di crittografare l'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a177d-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a177d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a177d-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a177d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a177d-105">DESCRIPTION</span></span>
<span data-ttu-id="a177d-106">Il cmdlet **Enable-AzDataLakeStoreKeyVault** tenta di abilitare un Vault Key gestito dall'utente per la crittografia dell'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a177d-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a177d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a177d-107">EXAMPLES</span></span>

### <span data-ttu-id="a177d-108">Esempio 1: abilitare il Vault chiave per l'account di ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="a177d-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="a177d-109">Questo comando tenta di abilitare l'archiviazione delle chiavi gestite dall'utente per l'account di data Lake Store denominato ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="a177d-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="a177d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a177d-110">PARAMETERS</span></span>

### <span data-ttu-id="a177d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a177d-111">-Account</span></span>
<span data-ttu-id="a177d-112">L'account di data Lake Store per abilitare l'archiviazione delle chiavi gestite dall'utente per</span><span class="sxs-lookup"><span data-stu-id="a177d-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="a177d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a177d-113">-DefaultProfile</span></span>
<span data-ttu-id="a177d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a177d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a177d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a177d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a177d-116">Nome del gruppo di risorse associato all'account.</span><span class="sxs-lookup"><span data-stu-id="a177d-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="a177d-117">Se non specificato, tenterà di essere individuato.</span><span class="sxs-lookup"><span data-stu-id="a177d-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="a177d-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a177d-118">-Confirm</span></span>
<span data-ttu-id="a177d-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a177d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a177d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a177d-120">-WhatIf</span></span>
<span data-ttu-id="a177d-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a177d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a177d-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a177d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a177d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a177d-123">CommonParameters</span></span>
<span data-ttu-id="a177d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a177d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a177d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a177d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a177d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a177d-126">INPUTS</span></span>

### <span data-ttu-id="a177d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a177d-127">System.String</span></span>

## <span data-ttu-id="a177d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a177d-128">OUTPUTS</span></span>

### <span data-ttu-id="a177d-129">System. void</span><span class="sxs-lookup"><span data-stu-id="a177d-129">System.Void</span></span>

## <span data-ttu-id="a177d-130">Note</span><span class="sxs-lookup"><span data-stu-id="a177d-130">NOTES</span></span>

## <span data-ttu-id="a177d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a177d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a177d-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a177d-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="a177d-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a177d-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

