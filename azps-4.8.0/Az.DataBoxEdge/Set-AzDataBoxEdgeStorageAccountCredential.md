---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190296"
---
# <span data-ttu-id="0bfe4-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0bfe4-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0bfe4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bfe4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfe4-103">Imposta le credenziali dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="0bfe4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bfe4-104">SYNTAX</span></span>

### <span data-ttu-id="0bfe4-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bfe4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bfe4-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bfe4-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bfe4-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bfe4-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bfe4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bfe4-108">DESCRIPTION</span></span>
<span data-ttu-id="0bfe4-109">Il cmdlet **set-AzDataBoxEdgeStorageAccountCredential** aggiorna le credenziali dell'account di archiviazione corrispondenti a un account di archiviazione nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="0bfe4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bfe4-110">EXAMPLES</span></span>

### <span data-ttu-id="0bfe4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0bfe4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="0bfe4-112">Consente di ruotare i tasti di scelta per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0bfe4-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="0bfe4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bfe4-113">PARAMETERS</span></span>

### <span data-ttu-id="0bfe4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bfe4-114">-AsJob</span></span>
<span data-ttu-id="0bfe4-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0bfe4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bfe4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfe4-116">-DefaultProfile</span></span>
<span data-ttu-id="0bfe4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bfe4-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0bfe4-118">-DeviceName</span></span>
<span data-ttu-id="0bfe4-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="0bfe4-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe4-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0bfe4-120">-EncryptionKey</span></span>
<span data-ttu-id="0bfe4-121">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="0bfe4-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="0bfe4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bfe4-122">-InputObject</span></span>
<span data-ttu-id="0bfe4-123">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="0bfe4-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bfe4-124">-Name</span></span>
<span data-ttu-id="0bfe4-125">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="0bfe4-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bfe4-126">-ResourceGroupName</span></span>
<span data-ttu-id="0bfe4-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0bfe4-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bfe4-128">-ResourceId</span></span>
<span data-ttu-id="0bfe4-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bfe4-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe4-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="0bfe4-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="0bfe4-131">Immettere il codice di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0bfe4-131">provide storage account access key</span></span>

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

### <span data-ttu-id="0bfe4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bfe4-132">-Confirm</span></span>
<span data-ttu-id="0bfe4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bfe4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bfe4-134">-WhatIf</span></span>
<span data-ttu-id="0bfe4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bfe4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bfe4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfe4-137">CommonParameters</span></span>
<span data-ttu-id="0bfe4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfe4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfe4-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bfe4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfe4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bfe4-140">INPUTS</span></span>

### <span data-ttu-id="0bfe4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0bfe4-141">System.String</span></span>

### <span data-ttu-id="0bfe4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0bfe4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0bfe4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bfe4-143">OUTPUTS</span></span>

### <span data-ttu-id="0bfe4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0bfe4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0bfe4-145">Note</span><span class="sxs-lookup"><span data-stu-id="0bfe4-145">NOTES</span></span>

## <span data-ttu-id="0bfe4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bfe4-146">RELATED LINKS</span></span>
