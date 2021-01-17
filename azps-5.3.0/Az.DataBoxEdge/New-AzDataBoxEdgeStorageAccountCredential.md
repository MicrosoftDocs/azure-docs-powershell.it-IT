---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487700"
---
# <span data-ttu-id="b350c-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b350c-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="b350c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b350c-102">SYNOPSIS</span></span>
<span data-ttu-id="b350c-103">Crea nuove credenziali per un account di archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b350c-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="b350c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b350c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b350c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b350c-105">DESCRIPTION</span></span>
<span data-ttu-id="b350c-106">Il cmdlet **New-AzDataBoxEdgeStorageAccountCredential** crea una nuova credenziale dell'account di archiviazione Edge per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="b350c-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="b350c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b350c-107">EXAMPLES</span></span>

### <span data-ttu-id="b350c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b350c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="b350c-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b350c-109">PARAMETERS</span></span>

### <span data-ttu-id="b350c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b350c-110">-AsJob</span></span>
<span data-ttu-id="b350c-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b350c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b350c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b350c-112">-DefaultProfile</span></span>
<span data-ttu-id="b350c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b350c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b350c-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b350c-114">-DeviceName</span></span>
<span data-ttu-id="b350c-115">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="b350c-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b350c-116">-EncryptionKey</span></span>
<span data-ttu-id="b350c-117">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="b350c-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b350c-118">-Name</span></span>
<span data-ttu-id="b350c-119">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="b350c-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b350c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b350c-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b350c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="b350c-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="b350c-123">Immettere il codice di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b350c-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b350c-124">-StorageAccountType</span></span>
<span data-ttu-id="b350c-125">Possibile tipo di accesso allo spazio di archiviazione GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="b350c-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b350c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b350c-126">-Confirm</span></span>
<span data-ttu-id="b350c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b350c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b350c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b350c-128">-WhatIf</span></span>
<span data-ttu-id="b350c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b350c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b350c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b350c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b350c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b350c-131">CommonParameters</span></span>
<span data-ttu-id="b350c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b350c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b350c-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b350c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b350c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b350c-134">INPUTS</span></span>

### <span data-ttu-id="b350c-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b350c-135">None</span></span>

## <span data-ttu-id="b350c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b350c-136">OUTPUTS</span></span>

### <span data-ttu-id="b350c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b350c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="b350c-138">Note</span><span class="sxs-lookup"><span data-stu-id="b350c-138">NOTES</span></span>

## <span data-ttu-id="b350c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b350c-139">RELATED LINKS</span></span>
