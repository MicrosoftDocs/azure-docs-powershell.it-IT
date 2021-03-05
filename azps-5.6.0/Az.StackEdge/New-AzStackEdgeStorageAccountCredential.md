---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: a9bb0e844101c4d21db52c2f7852e3b548d283cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002925"
---
# <span data-ttu-id="011e6-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="011e6-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="011e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="011e6-102">SYNOPSIS</span></span>
<span data-ttu-id="011e6-103">Crea nuove credenziali per un account di archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="011e6-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="011e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="011e6-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="011e6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="011e6-105">DESCRIPTION</span></span>
<span data-ttu-id="011e6-106">Il cmdlet **New-AzStackEdgeStorageAccountCredential** crea una nuova credenziali dell'account di archiviazione Edge per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="011e6-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="011e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="011e6-107">EXAMPLES</span></span>

### <span data-ttu-id="011e6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="011e6-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="011e6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="011e6-109">PARAMETERS</span></span>

### <span data-ttu-id="011e6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="011e6-110">-AsJob</span></span>
<span data-ttu-id="011e6-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="011e6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="011e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011e6-112">-DefaultProfile</span></span>
<span data-ttu-id="011e6-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="011e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011e6-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="011e6-114">-DeviceName</span></span>
<span data-ttu-id="011e6-115">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="011e6-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011e6-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="011e6-116">-EncryptionKey</span></span>
<span data-ttu-id="011e6-117">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="011e6-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="011e6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="011e6-118">-Name</span></span>
<span data-ttu-id="011e6-119">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="011e6-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="011e6-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="011e6-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011e6-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="011e6-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="011e6-123">fornire la chiave di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="011e6-123">provide storage account access key</span></span>

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

### <span data-ttu-id="011e6-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="011e6-124">-StorageAccountType</span></span>
<span data-ttu-id="011e6-125">Tipo di accesso di archiviazione possibile GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="011e6-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="011e6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="011e6-126">-Confirm</span></span>
<span data-ttu-id="011e6-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="011e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="011e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011e6-128">-WhatIf</span></span>
<span data-ttu-id="011e6-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="011e6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="011e6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="011e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="011e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011e6-131">CommonParameters</span></span>
<span data-ttu-id="011e6-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011e6-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="011e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011e6-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="011e6-134">INPUTS</span></span>

### <span data-ttu-id="011e6-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="011e6-135">None</span></span>

## <span data-ttu-id="011e6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="011e6-136">OUTPUTS</span></span>

### <span data-ttu-id="011e6-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="011e6-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="011e6-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="011e6-138">NOTES</span></span>

## <span data-ttu-id="011e6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="011e6-139">RELATED LINKS</span></span>
