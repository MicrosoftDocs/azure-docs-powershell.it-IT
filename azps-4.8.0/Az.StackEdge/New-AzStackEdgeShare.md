---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190045"
---
# <span data-ttu-id="08ade-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="08ade-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="08ade-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08ade-102">SYNOPSIS</span></span>
<span data-ttu-id="08ade-103">Crea una nuova condivisione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08ade-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="08ade-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08ade-104">SYNTAX</span></span>

### <span data-ttu-id="08ade-105">SmbParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08ade-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08ade-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ade-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08ade-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ade-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08ade-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ade-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08ade-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08ade-109">DESCRIPTION</span></span>
<span data-ttu-id="08ade-110">Il cmdlet **New-AzStackEdgeShare** crea una nuova condivisione nel dispositivo bordo stack.</span><span class="sxs-lookup"><span data-stu-id="08ade-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="08ade-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08ade-111">EXAMPLES</span></span>

### <span data-ttu-id="08ade-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08ade-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="08ade-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08ade-113">PARAMETERS</span></span>

### <span data-ttu-id="08ade-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08ade-114">-AsJob</span></span>
<span data-ttu-id="08ade-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="08ade-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08ade-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="08ade-116">-ClientAccessRight</span></span>
<span data-ttu-id="08ade-117">Accesso in lettura/scrittura per ClientID, ad esempio: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="08ade-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="08ade-118">-CloudShare</span></span>
<span data-ttu-id="08ade-119">Specificare il nome della risorsa di StorageAccountCredential esistente</span><span class="sxs-lookup"><span data-stu-id="08ade-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="08ade-120">-ContainerName</span></span>
<span data-ttu-id="08ade-121">Nome contenitore (in base al formato dati specificato, rappresenta il nome di file Azure/Pageblob/BLOB blocco)</span><span class="sxs-lookup"><span data-stu-id="08ade-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="08ade-122">-DataFormat</span></span>
<span data-ttu-id="08ade-123">Impostare il formato dati ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="08ade-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ade-124">-DefaultProfile</span></span>
<span data-ttu-id="08ade-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08ade-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ade-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="08ade-126">-DeviceName</span></span>
<span data-ttu-id="08ade-127">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="08ade-127">Device Name</span></span>

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

### <span data-ttu-id="08ade-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="08ade-128">-Name</span></span>
<span data-ttu-id="08ade-129">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="08ade-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="08ade-130">-NFS</span></span>
<span data-ttu-id="08ade-131">AccessProtocol in caso di creazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="08ade-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ade-132">-ResourceGroupName</span></span>
<span data-ttu-id="08ade-133">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="08ade-133">Resource Group Name</span></span>

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

### <span data-ttu-id="08ade-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="08ade-134">-SMB</span></span>
<span data-ttu-id="08ade-135">AccessProtocol in caso di creazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="08ade-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="08ade-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="08ade-137">Specificare il nome della risorsa di StorageAccountCredential esistente</span><span class="sxs-lookup"><span data-stu-id="08ade-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="08ade-138">-UserAccessRight</span></span>
<span data-ttu-id="08ade-139">consente di accedere a destra insieme ai nomi utente esistenti per accedere ai tipi di condivisione SMB, ad esempio: @ (@ {"username" = "nome utente-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizzato "})</span><span class="sxs-lookup"><span data-stu-id="08ade-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ade-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08ade-140">-Confirm</span></span>
<span data-ttu-id="08ade-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08ade-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ade-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ade-142">-WhatIf</span></span>
<span data-ttu-id="08ade-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08ade-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08ade-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08ade-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ade-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ade-145">CommonParameters</span></span>
<span data-ttu-id="08ade-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ade-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ade-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08ade-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ade-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08ade-148">INPUTS</span></span>

### <span data-ttu-id="08ade-149">System. String</span><span class="sxs-lookup"><span data-stu-id="08ade-149">System.String</span></span>

## <span data-ttu-id="08ade-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08ade-150">OUTPUTS</span></span>

### <span data-ttu-id="08ade-151">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="08ade-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="08ade-152">Note</span><span class="sxs-lookup"><span data-stu-id="08ade-152">NOTES</span></span>

## <span data-ttu-id="08ade-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08ade-153">RELATED LINKS</span></span>