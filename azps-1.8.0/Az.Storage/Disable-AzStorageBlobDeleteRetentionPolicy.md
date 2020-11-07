---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: b086703ba8466c6d67e297002e2127a092175c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676656"
---
# <span data-ttu-id="7e218-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e218-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7e218-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e218-102">SYNOPSIS</span></span>
<span data-ttu-id="7e218-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e218-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7e218-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e218-104">SYNTAX</span></span>

### <span data-ttu-id="7e218-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e218-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e218-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7e218-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e218-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="7e218-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e218-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e218-108">DESCRIPTION</span></span>
<span data-ttu-id="7e218-109">Il cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e218-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7e218-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e218-110">EXAMPLES</span></span>

### <span data-ttu-id="7e218-111">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="7e218-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="7e218-112">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="7e218-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="7e218-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e218-113">PARAMETERS</span></span>

### <span data-ttu-id="7e218-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e218-114">-DefaultProfile</span></span>
<span data-ttu-id="7e218-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e218-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e218-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e218-116">-PassThru</span></span>
<span data-ttu-id="7e218-117">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="7e218-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="7e218-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e218-118">-ResourceGroupName</span></span>
<span data-ttu-id="7e218-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e218-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e218-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e218-120">-ResourceId</span></span>
<span data-ttu-id="7e218-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="7e218-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="7e218-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e218-122">-StorageAccount</span></span>
<span data-ttu-id="7e218-123">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e218-123">Storage account object</span></span>

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

### <span data-ttu-id="7e218-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e218-124">-StorageAccountName</span></span>
<span data-ttu-id="7e218-125">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e218-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="7e218-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e218-126">-Confirm</span></span>
<span data-ttu-id="7e218-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e218-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e218-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e218-128">-WhatIf</span></span>
<span data-ttu-id="7e218-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e218-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e218-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e218-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e218-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e218-131">CommonParameters</span></span>
<span data-ttu-id="7e218-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e218-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e218-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e218-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e218-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e218-134">INPUTS</span></span>

### <span data-ttu-id="7e218-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e218-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7e218-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7e218-136">System.String</span></span>

## <span data-ttu-id="7e218-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e218-137">OUTPUTS</span></span>

### <span data-ttu-id="7e218-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e218-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7e218-139">Note</span><span class="sxs-lookup"><span data-stu-id="7e218-139">NOTES</span></span>

## <span data-ttu-id="7e218-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e218-140">RELATED LINKS</span></span>
