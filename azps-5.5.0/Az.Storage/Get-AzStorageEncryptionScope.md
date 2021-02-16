---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178199"
---
# <span data-ttu-id="71859-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71859-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="71859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71859-102">SYNOPSIS</span></span>
<span data-ttu-id="71859-103">Ottenere o elencare gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="71859-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="71859-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71859-104">SYNTAX</span></span>

### <span data-ttu-id="71859-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71859-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71859-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="71859-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71859-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71859-107">DESCRIPTION</span></span>
<span data-ttu-id="71859-108">Il cmdlet **Get-AzStorageEncryptionScope** ottiene o elenca gli ambiti di crittografia da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="71859-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="71859-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71859-109">EXAMPLES</span></span>

### <span data-ttu-id="71859-110">Esempio 1: Ottenere un singolo ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="71859-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="71859-111">Questo comando ottiene un singolo ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="71859-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="71859-112">Esempio 2: Elencare tutti gli ambiti di crittografia di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="71859-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="71859-113">Questo comando elenca tutti gli ambiti di crittografia di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="71859-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="71859-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71859-114">PARAMETERS</span></span>

### <span data-ttu-id="71859-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71859-115">-DefaultProfile</span></span>
<span data-ttu-id="71859-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71859-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71859-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="71859-117">-EncryptionScopeName</span></span>
<span data-ttu-id="71859-118">Nome Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71859-118">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="71859-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71859-119">-ResourceGroupName</span></span>
<span data-ttu-id="71859-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71859-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="71859-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="71859-121">-StorageAccount</span></span>
<span data-ttu-id="71859-122">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="71859-122">Storage account object</span></span>

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

### <span data-ttu-id="71859-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71859-123">-StorageAccountName</span></span>
<span data-ttu-id="71859-124">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="71859-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="71859-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71859-125">CommonParameters</span></span>
<span data-ttu-id="71859-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71859-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71859-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71859-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71859-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="71859-128">INPUTS</span></span>

### <span data-ttu-id="71859-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71859-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="71859-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71859-130">OUTPUTS</span></span>

### <span data-ttu-id="71859-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71859-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="71859-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="71859-132">NOTES</span></span>

## <span data-ttu-id="71859-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71859-133">RELATED LINKS</span></span>
