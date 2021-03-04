---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8c31f5f97b723db63253165e21d2abea220f18d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971293"
---
# <span data-ttu-id="a8120-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a8120-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a8120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8120-102">SYNOPSIS</span></span>
<span data-ttu-id="a8120-103">Aggiorna la condivisione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8120-103">Updates the share for a device.</span></span>

## <span data-ttu-id="a8120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8120-104">SYNTAX</span></span>

### <span data-ttu-id="a8120-105">SmbParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8120-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8120-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8120-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8120-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8120-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8120-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8120-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8120-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8120-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8120-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8120-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8120-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8120-111">DESCRIPTION</span></span>
<span data-ttu-id="a8120-112">Questo **set-AzDataBoxEdgeShare** sostituirà i diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="a8120-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="a8120-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8120-113">EXAMPLES</span></span>

### <span data-ttu-id="a8120-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8120-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="a8120-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a8120-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="a8120-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8120-116">PARAMETERS</span></span>

### <span data-ttu-id="a8120-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8120-117">-AsJob</span></span>
<span data-ttu-id="a8120-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8120-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8120-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="a8120-119">-ClientAccessRight</span></span>
<span data-ttu-id="a8120-120">Accesso di lettura/scrittura per id client, ad esempio:@(@{"Id Client"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="a8120-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8120-121">-DefaultProfile</span></span>
<span data-ttu-id="a8120-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8120-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8120-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a8120-123">-DeviceName</span></span>
<span data-ttu-id="a8120-124">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a8120-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8120-125">-InputObject</span></span>
<span data-ttu-id="a8120-126">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="a8120-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a8120-127">-Name</span></span>
<span data-ttu-id="a8120-128">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a8120-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8120-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8120-130">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a8120-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8120-131">-ResourceId</span></span>
<span data-ttu-id="a8120-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8120-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="a8120-133">-UserAccessRight</span></span>
<span data-ttu-id="a8120-134">fornire l'accesso direttamente insieme ai nomi utente esistenti per accedere ai tipi di condivisione SMB, Ad esempio: @(@{"Username"="nome-utente-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="a8120-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8120-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8120-135">-Confirm</span></span>
<span data-ttu-id="a8120-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8120-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8120-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8120-137">-WhatIf</span></span>
<span data-ttu-id="a8120-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8120-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8120-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8120-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8120-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8120-140">CommonParameters</span></span>
<span data-ttu-id="a8120-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8120-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8120-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8120-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8120-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8120-143">INPUTS</span></span>

### <span data-ttu-id="a8120-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a8120-144">System.String</span></span>

### <span data-ttu-id="a8120-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a8120-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a8120-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8120-146">OUTPUTS</span></span>

### <span data-ttu-id="a8120-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a8120-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a8120-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8120-148">NOTES</span></span>

## <span data-ttu-id="a8120-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8120-149">RELATED LINKS</span></span>
