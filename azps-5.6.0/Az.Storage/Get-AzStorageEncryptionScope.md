---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: 02d91338063a1c06654fa30cbbf584a6f62ea34a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981518"
---
# <span data-ttu-id="7486c-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="7486c-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="7486c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7486c-102">SYNOPSIS</span></span>
<span data-ttu-id="7486c-103">Ottenere o elencare gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7486c-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="7486c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7486c-104">SYNTAX</span></span>

### <span data-ttu-id="7486c-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7486c-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7486c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7486c-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7486c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7486c-107">DESCRIPTION</span></span>
<span data-ttu-id="7486c-108">Il cmdlet **Get-AzStorageEncryptionScope** ottiene o elenca gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7486c-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="7486c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7486c-109">EXAMPLES</span></span>

### <span data-ttu-id="7486c-110">Esempio 1: Ottenere un singolo ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="7486c-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="7486c-111">Questo comando ottiene un singolo ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="7486c-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="7486c-112">Esempio 2: Elencare tutti gli ambiti di crittografia di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7486c-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="7486c-113">Questo comando elenca tutti gli ambiti di crittografia di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7486c-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="7486c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7486c-114">PARAMETERS</span></span>

### <span data-ttu-id="7486c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7486c-115">-DefaultProfile</span></span>
<span data-ttu-id="7486c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7486c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7486c-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="7486c-117">-EncryptionScopeName</span></span>
<span data-ttu-id="7486c-118">Nome Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="7486c-118">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="7486c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7486c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7486c-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7486c-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="7486c-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7486c-121">-StorageAccount</span></span>
<span data-ttu-id="7486c-122">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7486c-122">Storage account object</span></span>

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

### <span data-ttu-id="7486c-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7486c-123">-StorageAccountName</span></span>
<span data-ttu-id="7486c-124">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7486c-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="7486c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7486c-125">CommonParameters</span></span>
<span data-ttu-id="7486c-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7486c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7486c-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7486c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7486c-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="7486c-128">INPUTS</span></span>

### <span data-ttu-id="7486c-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7486c-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7486c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7486c-130">OUTPUTS</span></span>

### <span data-ttu-id="7486c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="7486c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="7486c-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="7486c-132">NOTES</span></span>

## <span data-ttu-id="7486c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7486c-133">RELATED LINKS</span></span>
