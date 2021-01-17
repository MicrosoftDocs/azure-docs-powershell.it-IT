---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474829"
---
# <span data-ttu-id="4a127-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4a127-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="4a127-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a127-102">SYNOPSIS</span></span>
<span data-ttu-id="4a127-103">Ottenere o elencare gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a127-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="4a127-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a127-104">SYNTAX</span></span>

### <span data-ttu-id="4a127-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a127-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a127-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4a127-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a127-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a127-107">DESCRIPTION</span></span>
<span data-ttu-id="4a127-108">Il cmdlet **Get-AzStorageEncryptionScope** Ottiene o elenca gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a127-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="4a127-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a127-109">EXAMPLES</span></span>

### <span data-ttu-id="4a127-110">Esempio 1: ottenere un singolo ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="4a127-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="4a127-111">Questo comando ottiene un singolo ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4a127-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="4a127-112">Esempio 2: elencare tutti gli ambiti di crittografia di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a127-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="4a127-113">Questo comando elenca tutti gli ambiti di crittografia di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a127-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="4a127-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a127-114">PARAMETERS</span></span>

### <span data-ttu-id="4a127-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a127-115">-DefaultProfile</span></span>
<span data-ttu-id="4a127-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a127-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a127-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="4a127-117">-EncryptionScopeName</span></span>
<span data-ttu-id="4a127-118">Nome EncryptionScope di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4a127-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a127-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a127-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a127-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a127-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a127-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a127-121">-StorageAccount</span></span>
<span data-ttu-id="4a127-122">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a127-122">Storage account object</span></span>

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

### <span data-ttu-id="4a127-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a127-123">-StorageAccountName</span></span>
<span data-ttu-id="4a127-124">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a127-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="4a127-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a127-125">CommonParameters</span></span>
<span data-ttu-id="4a127-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a127-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a127-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a127-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a127-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a127-128">INPUTS</span></span>

### <span data-ttu-id="4a127-129">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a127-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4a127-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a127-130">OUTPUTS</span></span>

### <span data-ttu-id="4a127-131">Microsoft. Azure. Commands. Management. storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4a127-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="4a127-132">Note</span><span class="sxs-lookup"><span data-stu-id="4a127-132">NOTES</span></span>

## <span data-ttu-id="4a127-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a127-133">RELATED LINKS</span></span>
