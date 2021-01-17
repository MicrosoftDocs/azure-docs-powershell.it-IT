---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474013"
---
# <span data-ttu-id="f95ac-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="f95ac-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="f95ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f95ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f95ac-103">Ottiene l'elenco dei Vault di backup degli account di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="f95ac-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="f95ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f95ac-104">SYNTAX</span></span>

### <span data-ttu-id="f95ac-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f95ac-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95ac-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f95ac-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95ac-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f95ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f95ac-108">DESCRIPTION</span></span>
<span data-ttu-id="f95ac-109">Il cmdlet **Get-AzNetAppFilesVault** Ottiene l'elenco degli archivi di backup degli account di ANF.</span><span class="sxs-lookup"><span data-stu-id="f95ac-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="f95ac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f95ac-110">EXAMPLES</span></span>

### <span data-ttu-id="f95ac-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f95ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="f95ac-112">Questo comando ottiene un elenco dei Vault di backup per Azure NetappFiles (ANF) account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="f95ac-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="f95ac-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f95ac-113">PARAMETERS</span></span>

### <span data-ttu-id="f95ac-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f95ac-114">-AccountName</span></span>
<span data-ttu-id="f95ac-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="f95ac-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95ac-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f95ac-116">-AccountObject</span></span>
<span data-ttu-id="f95ac-117">Account per il nuovo oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="f95ac-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95ac-118">-DefaultProfile</span></span>
<span data-ttu-id="f95ac-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f95ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="f95ac-121">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f95ac-121">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95ac-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f95ac-122">-ResourceId</span></span>
<span data-ttu-id="f95ac-123">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="f95ac-123">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95ac-124">CommonParameters</span></span>
<span data-ttu-id="f95ac-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95ac-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f95ac-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95ac-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f95ac-127">INPUTS</span></span>

### <span data-ttu-id="f95ac-128">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f95ac-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f95ac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f95ac-129">System.String</span></span>

## <span data-ttu-id="f95ac-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f95ac-130">OUTPUTS</span></span>

### <span data-ttu-id="f95ac-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f95ac-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f95ac-132">Note</span><span class="sxs-lookup"><span data-stu-id="f95ac-132">NOTES</span></span>

## <span data-ttu-id="f95ac-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f95ac-133">RELATED LINKS</span></span>
