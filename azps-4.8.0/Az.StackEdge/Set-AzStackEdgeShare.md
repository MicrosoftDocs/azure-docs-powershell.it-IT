---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191157"
---
# <span data-ttu-id="a89f6-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a89f6-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="a89f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a89f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a89f6-103">Aggiorna la condivisione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a89f6-103">Updates the share for a device.</span></span>

## <span data-ttu-id="a89f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a89f6-104">SYNTAX</span></span>

### <span data-ttu-id="a89f6-105">SmbParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a89f6-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89f6-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89f6-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89f6-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89f6-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89f6-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89f6-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89f6-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89f6-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89f6-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89f6-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a89f6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a89f6-111">DESCRIPTION</span></span>
<span data-ttu-id="a89f6-112">Questo **set-AzStackEdgeShare** sostituirà i diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="a89f6-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="a89f6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a89f6-113">EXAMPLES</span></span>

### <span data-ttu-id="a89f6-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a89f6-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="a89f6-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a89f6-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="a89f6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a89f6-116">PARAMETERS</span></span>

### <span data-ttu-id="a89f6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a89f6-117">-AsJob</span></span>
<span data-ttu-id="a89f6-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a89f6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a89f6-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="a89f6-119">-ClientAccessRight</span></span>
<span data-ttu-id="a89f6-120">Accesso in lettura/scrittura per ClientID, ad esempio: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="a89f6-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="a89f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89f6-121">-DefaultProfile</span></span>
<span data-ttu-id="a89f6-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a89f6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a89f6-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a89f6-123">-DeviceName</span></span>
<span data-ttu-id="a89f6-124">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a89f6-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89f6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a89f6-125">-InputObject</span></span>
<span data-ttu-id="a89f6-126">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="a89f6-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89f6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a89f6-127">-Name</span></span>
<span data-ttu-id="a89f6-128">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a89f6-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89f6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89f6-129">-ResourceGroupName</span></span>
<span data-ttu-id="a89f6-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a89f6-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89f6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a89f6-131">-ResourceId</span></span>
<span data-ttu-id="a89f6-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a89f6-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="a89f6-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="a89f6-133">-UserAccessRight</span></span>
<span data-ttu-id="a89f6-134">consente di accedere a destra insieme ai nomi utente esistenti per accedere ai tipi di condivisione SMB, ad esempio: @ (@ {"username" = "nome utente-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizzato "})</span><span class="sxs-lookup"><span data-stu-id="a89f6-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="a89f6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a89f6-135">-Confirm</span></span>
<span data-ttu-id="a89f6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a89f6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a89f6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89f6-137">-WhatIf</span></span>
<span data-ttu-id="a89f6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a89f6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a89f6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a89f6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a89f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89f6-140">CommonParameters</span></span>
<span data-ttu-id="a89f6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a89f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89f6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a89f6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89f6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a89f6-143">INPUTS</span></span>

### <span data-ttu-id="a89f6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a89f6-144">System.String</span></span>

### <span data-ttu-id="a89f6-145">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a89f6-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="a89f6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a89f6-146">OUTPUTS</span></span>

### <span data-ttu-id="a89f6-147">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a89f6-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="a89f6-148">Note</span><span class="sxs-lookup"><span data-stu-id="a89f6-148">NOTES</span></span>

## <span data-ttu-id="a89f6-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a89f6-149">RELATED LINKS</span></span>
