---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360009"
---
# <span data-ttu-id="c3d43-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c3d43-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c3d43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3d43-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d43-103">Crea un nuovo account di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="c3d43-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="c3d43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3d43-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d43-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3d43-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d43-106">Il cmdlet **New-AzNetAppFilesAccount** crea un account ANF.</span><span class="sxs-lookup"><span data-stu-id="c3d43-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="c3d43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3d43-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d43-108">Esempio 1: creare un account di ANF</span><span class="sxs-lookup"><span data-stu-id="c3d43-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="c3d43-109">Questo comando crea il nuovo account di ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="c3d43-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="c3d43-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3d43-110">PARAMETERS</span></span>

### <span data-ttu-id="c3d43-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c3d43-111">-ActiveDirectory</span></span>
<span data-ttu-id="c3d43-112">Matrice Hashtable che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="c3d43-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d43-113">-DefaultProfile</span></span>
<span data-ttu-id="c3d43-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d43-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c3d43-115">-Location</span></span>
<span data-ttu-id="c3d43-116">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="c3d43-116">The location of the resource</span></span>

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

### <span data-ttu-id="c3d43-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3d43-117">-Name</span></span>
<span data-ttu-id="c3d43-118">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="c3d43-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d43-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3d43-120">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="c3d43-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c3d43-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3d43-121">-Tag</span></span>
<span data-ttu-id="c3d43-122">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="c3d43-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3d43-123">-Confirm</span></span>
<span data-ttu-id="c3d43-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d43-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d43-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d43-125">-WhatIf</span></span>
<span data-ttu-id="c3d43-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3d43-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d43-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3d43-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d43-128">CommonParameters</span></span>
<span data-ttu-id="c3d43-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d43-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3d43-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d43-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3d43-131">INPUTS</span></span>

### <span data-ttu-id="c3d43-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3d43-132">None</span></span>

## <span data-ttu-id="c3d43-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3d43-133">OUTPUTS</span></span>

### <span data-ttu-id="c3d43-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c3d43-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c3d43-135">Note</span><span class="sxs-lookup"><span data-stu-id="c3d43-135">NOTES</span></span>

## <span data-ttu-id="c3d43-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3d43-136">RELATED LINKS</span></span>
