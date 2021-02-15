---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188879"
---
# <span data-ttu-id="43743-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43743-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="43743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43743-102">SYNOPSIS</span></span>
<span data-ttu-id="43743-103">Disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43743-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="43743-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43743-104">SYNTAX</span></span>

### <span data-ttu-id="43743-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43743-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43743-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="43743-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43743-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="43743-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43743-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43743-108">DESCRIPTION</span></span>
<span data-ttu-id="43743-109">Il cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43743-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="43743-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43743-110">EXAMPLES</span></span>

### <span data-ttu-id="43743-111">Esempio 1: Disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="43743-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="43743-112">Questo comando disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="43743-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="43743-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43743-113">PARAMETERS</span></span>

### <span data-ttu-id="43743-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43743-114">-DefaultProfile</span></span>
<span data-ttu-id="43743-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43743-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43743-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43743-116">-PassThru</span></span>
<span data-ttu-id="43743-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="43743-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="43743-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43743-118">-ResourceGroupName</span></span>
<span data-ttu-id="43743-119">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43743-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="43743-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43743-120">-ResourceId</span></span>
<span data-ttu-id="43743-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="43743-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43743-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="43743-122">-StorageAccount</span></span>
<span data-ttu-id="43743-123">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="43743-123">Storage account object</span></span>

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

### <span data-ttu-id="43743-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="43743-124">-StorageAccountName</span></span>
<span data-ttu-id="43743-125">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43743-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="43743-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43743-126">-Confirm</span></span>
<span data-ttu-id="43743-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43743-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43743-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43743-128">-WhatIf</span></span>
<span data-ttu-id="43743-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43743-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43743-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43743-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43743-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43743-131">CommonParameters</span></span>
<span data-ttu-id="43743-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43743-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43743-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43743-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43743-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="43743-134">INPUTS</span></span>

### <span data-ttu-id="43743-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43743-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="43743-136">System.String</span><span class="sxs-lookup"><span data-stu-id="43743-136">System.String</span></span>

## <span data-ttu-id="43743-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43743-137">OUTPUTS</span></span>

### <span data-ttu-id="43743-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43743-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="43743-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="43743-139">NOTES</span></span>

## <span data-ttu-id="43743-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43743-140">RELATED LINKS</span></span>
