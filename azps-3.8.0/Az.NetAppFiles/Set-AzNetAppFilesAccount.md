---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864182"
---
# <span data-ttu-id="272e0-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="272e0-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="272e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="272e0-102">SYNOPSIS</span></span>
<span data-ttu-id="272e0-103">Aggiorna un account di Azure NetApp file (ANF) con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="272e0-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="272e0-104">Utile per l'eliminazione di Active Directory associate.</span><span class="sxs-lookup"><span data-stu-id="272e0-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="272e0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="272e0-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="272e0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="272e0-106">DESCRIPTION</span></span>
<span data-ttu-id="272e0-107">Il cmdlet **set-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="272e0-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="272e0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="272e0-108">EXAMPLES</span></span>

### <span data-ttu-id="272e0-109">Esempio 1: modificare un account di ANF</span><span class="sxs-lookup"><span data-stu-id="272e0-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="272e0-110">Questo comando esegue un aggiornamento per l'account specifico.</span><span class="sxs-lookup"><span data-stu-id="272e0-110">This command performs an update on the given account.</span></span> <span data-ttu-id="272e0-111">L'assenza di Active Directory significa che verrà rimossa dall'account.</span><span class="sxs-lookup"><span data-stu-id="272e0-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="272e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="272e0-112">PARAMETERS</span></span>

### <span data-ttu-id="272e0-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="272e0-113">-ActiveDirectories</span></span>
<span data-ttu-id="272e0-114">Matrice Hashtable che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="272e0-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="272e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272e0-115">-DefaultProfile</span></span>
<span data-ttu-id="272e0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="272e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272e0-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="272e0-117">-Location</span></span>
<span data-ttu-id="272e0-118">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="272e0-118">The location of the resource</span></span>

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

### <span data-ttu-id="272e0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="272e0-119">-Name</span></span>
<span data-ttu-id="272e0-120">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="272e0-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="272e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="272e0-122">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="272e0-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="272e0-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="272e0-123">-Tag</span></span>
<span data-ttu-id="272e0-124">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="272e0-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="272e0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="272e0-125">-Confirm</span></span>
<span data-ttu-id="272e0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="272e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272e0-127">-WhatIf</span></span>
<span data-ttu-id="272e0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="272e0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="272e0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="272e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272e0-130">CommonParameters</span></span>
<span data-ttu-id="272e0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="272e0-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272e0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272e0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="272e0-133">INPUTS</span></span>

### <span data-ttu-id="272e0-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="272e0-134">None</span></span>

## <span data-ttu-id="272e0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="272e0-135">OUTPUTS</span></span>

### <span data-ttu-id="272e0-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="272e0-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="272e0-137">Note</span><span class="sxs-lookup"><span data-stu-id="272e0-137">NOTES</span></span>

## <span data-ttu-id="272e0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="272e0-138">RELATED LINKS</span></span>
