---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: a168b48089052ed8daa764407254d04084ece771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510643"
---
# <span data-ttu-id="24975-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="24975-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="24975-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24975-102">SYNOPSIS</span></span>
<span data-ttu-id="24975-103">Consente di consentire a un Vault Key gestito dall'utente di crittografare l'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="24975-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24975-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24975-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24975-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24975-105">DESCRIPTION</span></span>
<span data-ttu-id="24975-106">Il cmdlet **Enable-AzureRmDataLakeStoreKeyVault** tenta di abilitare un Vault Key gestito dall'utente per la crittografia dell'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="24975-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="24975-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24975-107">EXAMPLES</span></span>

### <span data-ttu-id="24975-108">Esempio 1: abilitare il Vault chiave per l'account di ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="24975-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="24975-109">Questo comando tenta di abilitare l'archiviazione delle chiavi gestite dall'utente per l'account di data Lake Store denominato ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="24975-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="24975-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24975-110">PARAMETERS</span></span>

### <span data-ttu-id="24975-111">-Account</span><span class="sxs-lookup"><span data-stu-id="24975-111">-Account</span></span>
<span data-ttu-id="24975-112">L'account di data Lake Store per abilitare l'archiviazione delle chiavi gestite dall'utente per</span><span class="sxs-lookup"><span data-stu-id="24975-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="24975-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24975-113">-ResourceGroupName</span></span>
<span data-ttu-id="24975-114">Nome del gruppo di risorse associato all'account.</span><span class="sxs-lookup"><span data-stu-id="24975-114">Name of resource group associated with the account.</span></span> <span data-ttu-id="24975-115">Se non specificato, tenterà di essere individuato.</span><span class="sxs-lookup"><span data-stu-id="24975-115">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="24975-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24975-116">-Confirm</span></span>
<span data-ttu-id="24975-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24975-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24975-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24975-118">-WhatIf</span></span>
<span data-ttu-id="24975-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24975-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24975-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24975-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24975-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24975-121">-DefaultProfile</span></span>
<span data-ttu-id="24975-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24975-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24975-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24975-123">CommonParameters</span></span>
<span data-ttu-id="24975-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24975-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24975-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24975-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24975-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24975-126">INPUTS</span></span>

### <span data-ttu-id="24975-127">System. String</span><span class="sxs-lookup"><span data-stu-id="24975-127">System.String</span></span>

## <span data-ttu-id="24975-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24975-128">OUTPUTS</span></span>

## <span data-ttu-id="24975-129">Note</span><span class="sxs-lookup"><span data-stu-id="24975-129">NOTES</span></span>

## <span data-ttu-id="24975-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24975-130">RELATED LINKS</span></span>

[<span data-ttu-id="24975-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24975-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="24975-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24975-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

