---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019217"
---
# <span data-ttu-id="bd20b-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd20b-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bd20b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd20b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd20b-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd20b-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd20b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd20b-104">SYNTAX</span></span>

### <span data-ttu-id="bd20b-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd20b-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd20b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bd20b-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd20b-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="bd20b-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd20b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd20b-108">DESCRIPTION</span></span>
<span data-ttu-id="bd20b-109">Il cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd20b-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd20b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd20b-110">EXAMPLES</span></span>

### <span data-ttu-id="bd20b-111">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="bd20b-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="bd20b-112">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="bd20b-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="bd20b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd20b-113">PARAMETERS</span></span>

### <span data-ttu-id="bd20b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd20b-114">-DefaultProfile</span></span>
<span data-ttu-id="bd20b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd20b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd20b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd20b-116">-PassThru</span></span>
<span data-ttu-id="bd20b-117">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bd20b-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="bd20b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd20b-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd20b-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd20b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd20b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd20b-120">-ResourceId</span></span>
<span data-ttu-id="bd20b-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="bd20b-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="bd20b-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd20b-122">-StorageAccount</span></span>
<span data-ttu-id="bd20b-123">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="bd20b-123">Storage account object</span></span>

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

### <span data-ttu-id="bd20b-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bd20b-124">-StorageAccountName</span></span>
<span data-ttu-id="bd20b-125">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bd20b-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="bd20b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd20b-126">-Confirm</span></span>
<span data-ttu-id="bd20b-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd20b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd20b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd20b-128">-WhatIf</span></span>
<span data-ttu-id="bd20b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd20b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd20b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd20b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd20b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd20b-131">CommonParameters</span></span>
<span data-ttu-id="bd20b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd20b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd20b-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd20b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd20b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd20b-134">INPUTS</span></span>

### <span data-ttu-id="bd20b-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd20b-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bd20b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bd20b-136">System.String</span></span>

## <span data-ttu-id="bd20b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd20b-137">OUTPUTS</span></span>

### <span data-ttu-id="bd20b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd20b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bd20b-139">Note</span><span class="sxs-lookup"><span data-stu-id="bd20b-139">NOTES</span></span>

## <span data-ttu-id="bd20b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd20b-140">RELATED LINKS</span></span>
