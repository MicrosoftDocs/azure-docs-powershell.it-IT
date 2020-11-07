---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: e6fa7a00218e52eae6b0323bc5e8ac25459986ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864181"
---
# <span data-ttu-id="1d5ae-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1d5ae-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="1d5ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5ae-103">Aggiorna un account di ANF (Azure NetApp files) in base ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="1d5ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d5ae-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="1d5ae-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d5ae-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d5ae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d5ae-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d5ae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d5ae-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d5ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d5ae-108">DESCRIPTION</span></span>
<span data-ttu-id="1d5ae-109">Il cmdlet **Update-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="1d5ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d5ae-110">EXAMPLES</span></span>

### <span data-ttu-id="1d5ae-111">Esempio 1: aggiorna un account di ANF</span><span class="sxs-lookup"><span data-stu-id="1d5ae-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="1d5ae-112">Questo comando esegue un aggiornamento nell'account specificato modificando i tag in quelli forniti.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="1d5ae-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d5ae-113">PARAMETERS</span></span>

### <span data-ttu-id="1d5ae-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="1d5ae-114">-ActiveDirectories</span></span>
<span data-ttu-id="1d5ae-115">Matrice Hashtable che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="1d5ae-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5ae-116">-DefaultProfile</span></span>
<span data-ttu-id="1d5ae-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d5ae-118">-InputObject</span></span>
<span data-ttu-id="1d5ae-119">L'oggetto account da aggiornare</span><span class="sxs-lookup"><span data-stu-id="1d5ae-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1d5ae-120">-Location</span></span>
<span data-ttu-id="1d5ae-121">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="1d5ae-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d5ae-122">-Name</span></span>
<span data-ttu-id="1d5ae-123">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="1d5ae-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d5ae-125">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1d5ae-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d5ae-126">-ResourceId</span></span>
<span data-ttu-id="1d5ae-127">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1d5ae-127">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d5ae-128">-Tag</span></span>
<span data-ttu-id="1d5ae-129">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="1d5ae-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d5ae-130">-Confirm</span></span>
<span data-ttu-id="1d5ae-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d5ae-132">-WhatIf</span></span>
<span data-ttu-id="1d5ae-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d5ae-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5ae-135">CommonParameters</span></span>
<span data-ttu-id="1d5ae-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1d5ae-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d5ae-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5ae-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d5ae-138">INPUTS</span></span>

### <span data-ttu-id="1d5ae-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1d5ae-139">None</span></span>

## <span data-ttu-id="1d5ae-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d5ae-140">OUTPUTS</span></span>

### <span data-ttu-id="1d5ae-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1d5ae-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1d5ae-142">Note</span><span class="sxs-lookup"><span data-stu-id="1d5ae-142">NOTES</span></span>

## <span data-ttu-id="1d5ae-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d5ae-143">RELATED LINKS</span></span>
