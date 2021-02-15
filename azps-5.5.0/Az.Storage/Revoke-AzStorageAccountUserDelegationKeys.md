---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188862"
---
# <span data-ttu-id="f0f95-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f0f95-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="f0f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0f95-102">SYNOPSIS</span></span>
<span data-ttu-id="f0f95-103">Revocare tutte le chiavi di delega utente di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0f95-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="f0f95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0f95-104">SYNTAX</span></span>

### <span data-ttu-id="f0f95-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0f95-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0f95-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f0f95-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0f95-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f0f95-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0f95-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0f95-108">DESCRIPTION</span></span>
<span data-ttu-id="f0f95-109">Il cmdlet **Revoke-AzStorageAccountUserDelegationKeys** revoca tutte le chiavi di delega utente di un account di archiviazione, quindi verrà revocato anche tutto il token di firma di accesso condiviso di identità dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0f95-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="f0f95-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0f95-110">EXAMPLES</span></span>

### <span data-ttu-id="f0f95-111">Esempio 1: Revocare tutte le chiavi di delega utente di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f0f95-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="f0f95-112">Questo esempio revoca tutte le chiavi di delega utente di un account di archiviazione, quindi verrà revocato anche tutto il token di firma di accesso condiviso di identità generato dalle chiavi di delega utente.</span><span class="sxs-lookup"><span data-stu-id="f0f95-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="f0f95-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0f95-113">PARAMETERS</span></span>

### <span data-ttu-id="f0f95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0f95-114">-DefaultProfile</span></span>
<span data-ttu-id="f0f95-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0f95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0f95-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0f95-116">-InputObject</span></span>
<span data-ttu-id="f0f95-117">Oggetto account di archiviazione restituito da Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f0f95-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f95-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0f95-118">-PassThru</span></span>
<span data-ttu-id="f0f95-119">In genere questo cmdlet non restituisce alcun output al completamento corretto, quindi forza il cmdlet a restituire un valore ($true) al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="f0f95-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="f0f95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0f95-120">-ResourceGroupName</span></span>
<span data-ttu-id="f0f95-121">Nome del gruppo di risorse che contiene la risorsa dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0f95-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="f0f95-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0f95-122">-ResourceId</span></span>
<span data-ttu-id="f0f95-123">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0f95-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f95-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f0f95-124">-StorageAccountName</span></span>
<span data-ttu-id="f0f95-125">Nome della risorsa dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0f95-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0f95-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0f95-126">-Confirm</span></span>
<span data-ttu-id="f0f95-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0f95-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0f95-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0f95-128">-WhatIf</span></span>
<span data-ttu-id="f0f95-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0f95-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0f95-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0f95-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0f95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0f95-131">CommonParameters</span></span>
<span data-ttu-id="f0f95-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0f95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0f95-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0f95-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0f95-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0f95-134">INPUTS</span></span>

### <span data-ttu-id="f0f95-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0f95-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f0f95-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f0f95-136">System.String</span></span>

## <span data-ttu-id="f0f95-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0f95-137">OUTPUTS</span></span>

### <span data-ttu-id="f0f95-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0f95-138">System.Boolean</span></span>

## <span data-ttu-id="f0f95-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0f95-139">NOTES</span></span>

## <span data-ttu-id="f0f95-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0f95-140">RELATED LINKS</span></span>
