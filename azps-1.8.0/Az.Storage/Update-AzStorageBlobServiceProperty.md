---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676465"
---
# <span data-ttu-id="f0e1d-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f0e1d-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="f0e1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e1d-103">Modifica le proprietà del servizio per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f0e1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0e1d-104">SYNTAX</span></span>

### <span data-ttu-id="f0e1d-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0e1d-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0e1d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f0e1d-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0e1d-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f0e1d-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0e1d-108">DESCRIPTION</span></span>
<span data-ttu-id="f0e1d-109">Il cmdlet **Update-AzStorageBlobServiceProperty** modifica le proprietà del servizio per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f0e1d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0e1d-110">EXAMPLES</span></span>

### <span data-ttu-id="f0e1d-111">Esempio 1: impostare il servizio BLOB DefaultServiceVersion su 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="f0e1d-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="f0e1d-112">Questo comando imposta il servizio DefaultServiceVersion di BLOB su 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="f0e1d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0e1d-113">PARAMETERS</span></span>

### <span data-ttu-id="f0e1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e1d-114">-DefaultProfile</span></span>
<span data-ttu-id="f0e1d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0e1d-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="f0e1d-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="f0e1d-117">Versione predefinita del servizio da impostare</span><span class="sxs-lookup"><span data-stu-id="f0e1d-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e1d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0e1d-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0e1d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0e1d-120">-ResourceId</span></span>
<span data-ttu-id="f0e1d-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f0e1d-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0e1d-122">-StorageAccount</span></span>
<span data-ttu-id="f0e1d-123">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f0e1d-123">Storage account object</span></span>

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

### <span data-ttu-id="f0e1d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f0e1d-124">-StorageAccountName</span></span>
<span data-ttu-id="f0e1d-125">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="f0e1d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0e1d-126">-Confirm</span></span>
<span data-ttu-id="f0e1d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e1d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e1d-128">-WhatIf</span></span>
<span data-ttu-id="f0e1d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e1d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e1d-131">CommonParameters</span></span>
<span data-ttu-id="f0e1d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e1d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e1d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0e1d-134">INPUTS</span></span>

### <span data-ttu-id="f0e1d-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0e1d-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f0e1d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e1d-136">System.String</span></span>

## <span data-ttu-id="f0e1d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0e1d-137">OUTPUTS</span></span>

### <span data-ttu-id="f0e1d-138">Microsoft. Azure. Commands. Management. storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f0e1d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="f0e1d-139">Note</span><span class="sxs-lookup"><span data-stu-id="f0e1d-139">NOTES</span></span>

## <span data-ttu-id="f0e1d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0e1d-140">RELATED LINKS</span></span>
