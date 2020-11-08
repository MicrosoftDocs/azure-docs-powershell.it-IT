---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193746"
---
# <span data-ttu-id="9e21c-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="9e21c-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="9e21c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e21c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e21c-103">Revocare tutte le chiavi di delega degli utenti di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e21c-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="9e21c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e21c-104">SYNTAX</span></span>

### <span data-ttu-id="9e21c-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e21c-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e21c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9e21c-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e21c-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9e21c-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e21c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e21c-108">DESCRIPTION</span></span>
<span data-ttu-id="9e21c-109">Il cmdlet **Revoke-AzStorageAccountUserDelegationKeys** revoca tutte le chiavi di delega degli utenti di un account di archiviazione, quindi verranno revocati anche tutti i token SAS identità dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e21c-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="9e21c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e21c-110">EXAMPLES</span></span>

### <span data-ttu-id="9e21c-111">Esempio 1: revocare tutte le chiavi di delega degli utenti di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9e21c-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="9e21c-112">Questo esempio revoca tutte le chiavi di delega degli utenti di un account di archiviazione, quindi verranno revocati anche tutti i token SAS Identity generati dalle chiavi di delega dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e21c-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="9e21c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e21c-113">PARAMETERS</span></span>

### <span data-ttu-id="9e21c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e21c-114">-DefaultProfile</span></span>
<span data-ttu-id="9e21c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e21c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e21c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e21c-116">-InputObject</span></span>
<span data-ttu-id="9e21c-117">Un oggetto account di archiviazione, restituito da Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="9e21c-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="9e21c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e21c-118">-PassThru</span></span>
<span data-ttu-id="9e21c-119">In genere questo cmdlet non restituisce alcun output al completamento corretto, questo parametro impone al cmdlet di restituire un valore ($true) al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="9e21c-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="9e21c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e21c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e21c-121">Nome del gruppo di risorse che contiene la risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e21c-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="9e21c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e21c-122">-ResourceId</span></span>
<span data-ttu-id="9e21c-123">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e21c-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="9e21c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9e21c-124">-StorageAccountName</span></span>
<span data-ttu-id="9e21c-125">Nome della risorsa dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e21c-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="9e21c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e21c-126">-Confirm</span></span>
<span data-ttu-id="9e21c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e21c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e21c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e21c-128">-WhatIf</span></span>
<span data-ttu-id="9e21c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e21c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e21c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e21c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e21c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e21c-131">CommonParameters</span></span>
<span data-ttu-id="9e21c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e21c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e21c-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e21c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e21c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e21c-134">INPUTS</span></span>

### <span data-ttu-id="9e21c-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e21c-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9e21c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e21c-136">System.String</span></span>

## <span data-ttu-id="9e21c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e21c-137">OUTPUTS</span></span>

### <span data-ttu-id="9e21c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e21c-138">System.Boolean</span></span>

## <span data-ttu-id="9e21c-139">Note</span><span class="sxs-lookup"><span data-stu-id="9e21c-139">NOTES</span></span>

## <span data-ttu-id="9e21c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e21c-140">RELATED LINKS</span></span>
