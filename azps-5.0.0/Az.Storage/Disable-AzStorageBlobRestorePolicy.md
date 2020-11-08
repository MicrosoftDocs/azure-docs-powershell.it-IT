---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193595"
---
# <span data-ttu-id="793ba-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="793ba-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="793ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="793ba-102">SYNOPSIS</span></span>
<span data-ttu-id="793ba-103">Disabilita i criteri di ripristino BLOB in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="793ba-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="793ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="793ba-104">SYNTAX</span></span>

### <span data-ttu-id="793ba-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="793ba-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="793ba-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="793ba-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="793ba-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="793ba-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793ba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="793ba-108">DESCRIPTION</span></span>
<span data-ttu-id="793ba-109">Il cmdlet **Disable-AzStorageBlobRestorePolicy Disabilita** i criteri di ripristino BLOB per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="793ba-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="793ba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="793ba-110">EXAMPLES</span></span>

### <span data-ttu-id="793ba-111">Esempio 1: Disabilita i criteri di ripristino BLOB per il servizio BLOB di archiviazione di Azure in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="793ba-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="793ba-112">Questo comando Disabilita i criteri di ripristino BLOB per il servizio BLOB di archiviazione di Azure in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="793ba-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="793ba-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="793ba-113">PARAMETERS</span></span>

### <span data-ttu-id="793ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793ba-114">-DefaultProfile</span></span>
<span data-ttu-id="793ba-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="793ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="793ba-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="793ba-116">-PassThru</span></span>
<span data-ttu-id="793ba-117">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="793ba-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="793ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="793ba-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="793ba-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="793ba-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="793ba-120">-ResourceId</span></span>
<span data-ttu-id="793ba-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="793ba-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="793ba-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="793ba-122">-StorageAccount</span></span>
<span data-ttu-id="793ba-123">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="793ba-123">Storage account object</span></span>

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

### <span data-ttu-id="793ba-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="793ba-124">-StorageAccountName</span></span>
<span data-ttu-id="793ba-125">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="793ba-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="793ba-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="793ba-126">-Confirm</span></span>
<span data-ttu-id="793ba-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="793ba-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793ba-128">-WhatIf</span></span>
<span data-ttu-id="793ba-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="793ba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="793ba-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="793ba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793ba-131">CommonParameters</span></span>
<span data-ttu-id="793ba-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793ba-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="793ba-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793ba-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="793ba-134">INPUTS</span></span>

### <span data-ttu-id="793ba-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="793ba-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="793ba-136">System. String</span><span class="sxs-lookup"><span data-stu-id="793ba-136">System.String</span></span>

## <span data-ttu-id="793ba-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="793ba-137">OUTPUTS</span></span>

### <span data-ttu-id="793ba-138">Microsoft. Azure. Commands. Management. storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="793ba-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="793ba-139">Note</span><span class="sxs-lookup"><span data-stu-id="793ba-139">NOTES</span></span>

## <span data-ttu-id="793ba-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="793ba-140">RELATED LINKS</span></span>
