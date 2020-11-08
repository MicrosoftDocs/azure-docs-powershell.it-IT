---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021017"
---
# <span data-ttu-id="a32d7-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a32d7-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a32d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a32d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a32d7-103">Crea nuove credenziali per un account di archiviazione Edge nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a32d7-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="a32d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a32d7-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a32d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a32d7-106">Il cmdlet **New-AzStackEdgeStorageAccountCredential** crea una nuova credenziale dell'account di archiviazione Edge per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="a32d7-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="a32d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a32d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a32d7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a32d7-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="a32d7-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a32d7-109">PARAMETERS</span></span>

### <span data-ttu-id="a32d7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a32d7-110">-AsJob</span></span>
<span data-ttu-id="a32d7-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a32d7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a32d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32d7-112">-DefaultProfile</span></span>
<span data-ttu-id="a32d7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a32d7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32d7-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a32d7-114">-DeviceName</span></span>
<span data-ttu-id="a32d7-115">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a32d7-115">Device Name</span></span>

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

### <span data-ttu-id="a32d7-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a32d7-116">-EncryptionKey</span></span>
<span data-ttu-id="a32d7-117">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="a32d7-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="a32d7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a32d7-118">-Name</span></span>
<span data-ttu-id="a32d7-119">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="a32d7-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="a32d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="a32d7-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a32d7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a32d7-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="a32d7-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="a32d7-123">Immettere il codice di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a32d7-123">provide storage account access key</span></span>

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

### <span data-ttu-id="a32d7-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a32d7-124">-StorageAccountType</span></span>
<span data-ttu-id="a32d7-125">Possibile tipo di accesso allo spazio di archiviazione GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="a32d7-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="a32d7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a32d7-126">-Confirm</span></span>
<span data-ttu-id="a32d7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a32d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32d7-128">-WhatIf</span></span>
<span data-ttu-id="a32d7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a32d7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a32d7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a32d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32d7-131">CommonParameters</span></span>
<span data-ttu-id="a32d7-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32d7-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a32d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32d7-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a32d7-134">INPUTS</span></span>

### <span data-ttu-id="a32d7-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a32d7-135">None</span></span>

## <span data-ttu-id="a32d7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a32d7-136">OUTPUTS</span></span>

### <span data-ttu-id="a32d7-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a32d7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a32d7-138">Note</span><span class="sxs-lookup"><span data-stu-id="a32d7-138">NOTES</span></span>

## <span data-ttu-id="a32d7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a32d7-139">RELATED LINKS</span></span>
