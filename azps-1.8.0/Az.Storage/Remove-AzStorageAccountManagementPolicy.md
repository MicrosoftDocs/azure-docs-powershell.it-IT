---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: d7290d44a1e6a08b79ccb5a0b5ff88ec482b4875
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676541"
---
# <span data-ttu-id="1b3ea-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1b3ea-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="1b3ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3ea-103">Rimuove i criteri di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="1b3ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b3ea-104">SYNTAX</span></span>

### <span data-ttu-id="1b3ea-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b3ea-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b3ea-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1b3ea-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b3ea-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1b3ea-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b3ea-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="1b3ea-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b3ea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b3ea-109">DESCRIPTION</span></span>
<span data-ttu-id="1b3ea-110">Il cmdlet **Remove-AzStorageAccountManagementPolicy** rimuove i criteri di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="1b3ea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b3ea-111">EXAMPLES</span></span>

### <span data-ttu-id="1b3ea-112">Esempio 1: rimuovere i criteri di gestione di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="1b3ea-113">Questo comando rimuove i criteri di gestione di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="1b3ea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b3ea-114">PARAMETERS</span></span>

### <span data-ttu-id="1b3ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3ea-115">-DefaultProfile</span></span>
<span data-ttu-id="1b3ea-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b3ea-117">-InputObject</span></span>
<span data-ttu-id="1b3ea-118">Oggetto di gestione da rimuovere</span><span class="sxs-lookup"><span data-stu-id="1b3ea-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3ea-119">-PassThru</span></span>
<span data-ttu-id="1b3ea-120">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1b3ea-121">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-121">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b3ea-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b3ea-124">-StorageAccount</span></span>
<span data-ttu-id="1b3ea-125">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1b3ea-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1b3ea-126">-StorageAccountName</span></span>
<span data-ttu-id="1b3ea-127">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1b3ea-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="1b3ea-129">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ea-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b3ea-130">-Confirm</span></span>
<span data-ttu-id="1b3ea-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b3ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b3ea-132">-WhatIf</span></span>
<span data-ttu-id="1b3ea-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b3ea-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b3ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3ea-135">CommonParameters</span></span>
<span data-ttu-id="1b3ea-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3ea-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3ea-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3ea-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b3ea-138">INPUTS</span></span>

### <span data-ttu-id="1b3ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1b3ea-139">System.String</span></span>

## <span data-ttu-id="1b3ea-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b3ea-140">OUTPUTS</span></span>

### <span data-ttu-id="1b3ea-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b3ea-141">System.Boolean</span></span>

## <span data-ttu-id="1b3ea-142">Note</span><span class="sxs-lookup"><span data-stu-id="1b3ea-142">NOTES</span></span>

## <span data-ttu-id="1b3ea-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b3ea-143">RELATED LINKS</span></span>
