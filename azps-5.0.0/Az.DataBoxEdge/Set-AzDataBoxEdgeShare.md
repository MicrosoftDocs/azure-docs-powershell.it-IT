---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298657"
---
# <span data-ttu-id="5724a-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5724a-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="5724a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5724a-102">SYNOPSIS</span></span>
<span data-ttu-id="5724a-103">Aggiorna la condivisione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5724a-103">Updates the share for a device.</span></span>

## <span data-ttu-id="5724a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5724a-104">SYNTAX</span></span>

### <span data-ttu-id="5724a-105">SmbParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5724a-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5724a-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="5724a-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5724a-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5724a-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5724a-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="5724a-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5724a-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5724a-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5724a-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5724a-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5724a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5724a-111">DESCRIPTION</span></span>
<span data-ttu-id="5724a-112">Questo **set-AzDataBoxEdgeShare** sostituirà i diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="5724a-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="5724a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5724a-113">EXAMPLES</span></span>

### <span data-ttu-id="5724a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5724a-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="5724a-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5724a-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="5724a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5724a-116">PARAMETERS</span></span>

### <span data-ttu-id="5724a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5724a-117">-AsJob</span></span>
<span data-ttu-id="5724a-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5724a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5724a-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="5724a-119">-ClientAccessRight</span></span>
<span data-ttu-id="5724a-120">Accesso in lettura/scrittura per ClientID, ad esempio: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="5724a-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="5724a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5724a-121">-DefaultProfile</span></span>
<span data-ttu-id="5724a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5724a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5724a-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5724a-123">-DeviceName</span></span>
<span data-ttu-id="5724a-124">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="5724a-124">Device Name</span></span>

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

### <span data-ttu-id="5724a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5724a-125">-InputObject</span></span>
<span data-ttu-id="5724a-126">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="5724a-126">Input Object</span></span>

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

### <span data-ttu-id="5724a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5724a-127">-Name</span></span>
<span data-ttu-id="5724a-128">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="5724a-128">Resource Name</span></span>

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

### <span data-ttu-id="5724a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5724a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5724a-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5724a-130">Resource Group Name</span></span>

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

### <span data-ttu-id="5724a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5724a-131">-ResourceId</span></span>
<span data-ttu-id="5724a-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5724a-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="5724a-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="5724a-133">-UserAccessRight</span></span>
<span data-ttu-id="5724a-134">consente di accedere a destra insieme ai nomi utente esistenti per accedere ai tipi di condivisione SMB, ad esempio: @ (@ {"username" = "nome utente-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizzato "})</span><span class="sxs-lookup"><span data-stu-id="5724a-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="5724a-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5724a-135">-Confirm</span></span>
<span data-ttu-id="5724a-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5724a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5724a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5724a-137">-WhatIf</span></span>
<span data-ttu-id="5724a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5724a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5724a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5724a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5724a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5724a-140">CommonParameters</span></span>
<span data-ttu-id="5724a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5724a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5724a-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5724a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5724a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5724a-143">INPUTS</span></span>

### <span data-ttu-id="5724a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5724a-144">System.String</span></span>

### <span data-ttu-id="5724a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5724a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="5724a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5724a-146">OUTPUTS</span></span>

### <span data-ttu-id="5724a-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5724a-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="5724a-148">Note</span><span class="sxs-lookup"><span data-stu-id="5724a-148">NOTES</span></span>

## <span data-ttu-id="5724a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5724a-149">RELATED LINKS</span></span>
